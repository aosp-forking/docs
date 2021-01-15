# AOSPK
## Official devices application

Submit your request to join the team: https://forms.gle/k967Pzrqd1PBSqQTA

Before you open a pull request to add your device into our list of official devices, you should know a few simple things:

### To turn into a maintainer of AOSPK:
1. - You must have a way to check your builds, on your own way, having the device, or send the builds for someone test. Completely blind and/or untested builds aren't allowed.
2. - Appliers that comproved have the device, will have the preference on taking the maintainship.
3. - You must have knowledge of git.
4. - You must do an unofficial build and make the device stable for daily usage before applying.
5. - You should have your device sources open for us take a look.
6. - You mustn't be a placeholder of another maintainer that was removed. The pull request that are considered of that kind won't be accepted.

### Maintainers conduct notes:
1. - The maintainers should upload theirs trees on https://github.com/AOSPK-Devices
2. - The maintainers should test every update before upload in our OTA.
3. - The maintainers must keep the authorship of Git commits on everything that they'll make a change, even it's your device tree, kernel or ROM sources. Lots of git commit --amend and force-pushes are acceptable.
4. - Relationships fights can be done in PM on Telegram or XDA.
5. - The maintainers also need to add **export CUSTOM_BUILD_TYPE=OFFICIAL** in their build environment so OTA app will be included.

### Hosting
Our files are hosted on the SourceForge server, you will receive the credentials when you join the team.

### Changelog
For each new version, you need to upload the changelog to this repository in the device specific folder.

The changelog file name must match the **.zip** file name and should end with **.txt**
Eg: **.zip** is **AOSPK-11-20200101-0000-beryllium.zip**, changelog file name should be **AOSPK-11-20200101-0000-beryllium.txt**

### 5. Over-the-air (OTA) updates
Our system is automatic, you should not worry about updating some script, just upload the new build to the FTP server and send a pull request with the changelog and also edit your device JSON file (**builds/device_codename.json**) in this repository.

Eg: Poco F1 is called **beryllium**, so the device JSON file is **builds/beryllium.json**

**Note:** New builds can take up to 30 minutes to appear on the site and in the OTA application.

### 6. JSON params

##### devices.json
| Param | Description | Required |
|--|--|--|
| name | Device name | Yes |
| brand | Device manufacturer | Yes |
| codename | Device codename, eg: beryllium | Yes |
| maintainer_name | Your name | Yes |
| maintainer_url | Your personal URL, eg: https://github.com/YouName or https://forum.xda-developers.com/member.php?u=YouID | No  |
| xda_thread | XDA thread URL, eg: https://forum.xda-developers.com/.../link | No |

##### builds/your_device_codename.json
| Param | Description | Required |
|--|--|--|
| datetime | ... | Yes |
| filename | Build file (.zip) name | Yes |
| id | Build file (.zip) md5 hash | Yes |
| romtype | OFFICIAL | Yes |
| size | Build file (.zip) size (in bytes) | Yes |
| url | URL | Yes |
| version | 11 | Yes |
