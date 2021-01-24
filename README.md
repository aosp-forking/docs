# AOSPK - The Kraken Project
## Official devices application

Submit your request to join the team: https://forms.gle/k967Pzrqd1PBSqQTA

Before you open a pull request to add your device into our list of official devices, you should know a few simple things:

### To turn into a maintainer of Kraken:
1. - You must have a way to check your builds, on your own way, having the device, or send the builds for someone test. Completely blind and/or untested builds aren't allowed.
2. - You must have knowledge of git.
3. - You must do an unofficial build and make the device stable for daily usage before applying.
4. - You should have your device sources open for us take a look.
5. - You mustn't be a placeholder of another maintainer that was removed. The pull request that are considered of that kind won't be accepted.

### Maintainers conduct notes:
1. - The maintainers should upload theirs trees on [AOSPK-Devices](https://github.com/AOSPK-Devices)
2. - The maintainers should test every update before upload in our OTA.
3. - The maintainers must keep the authorship of Git commits on everything that they'll make a change, even it's your device tree, kernel or ROM sources. Lots of git commit --amend and force-pushes are acceptable.
4. - Relationships fights can be done in PM on Telegram or XDA.
5. - The maintainers also need to add **export CUSTOM_BUILD_TYPE=OFFICIAL** in their build environment so OTA app will be included.

### Upload new buildings:
1. - Make sure the build has been tested and is working. Never do this without the building having been tested!
2. - Upload to our host on **SourceForge**. You can do this both from the terminal or the browser.
   - Terminal:
   - `scp Kraken-11-20200112-1303-beryllium.zip username@frs.sourceforge.net:/home/frs/p/aospk/youdevice`
3. - To make it available in our download center it is necessary to register the construction in the [AOSPK/official_devices](https://github.com/AOSPK/official_devices).
4. - Only after these steps will you be free to publish in channels, groups and XDA.

### Changelog
For each new version, you need to upload the changelog to this repository in the device specific folder.

The changelog file name must match the **.zip** file name and should end with **.txt**
Eg: **.zip**, **Kraken-11-20200112-1303-beryllium.zip**, changelog file name should be **Kraken-11-20200112-1303-beryllium.txt**

### Over-the-air (OTA) updates
Our system is automatic, you should not worry about updating some script, just upload the new build to the FTP server and send a pull request with the changelog and also edit your device JSON file **builds/device_codename.json**.

Eg: Poco F1 is called **beryllium**, so the device JSON file is **builds/beryllium.json**

**Note:** New builds can take up to 10 minutes to appear on the site and in the OTA application.

### JSON params
##### devices.json
| Param | Description |
|--|--|
| brand | Device manufacturer |
| name | Device name |
| codename | Device codename, eg: beryllium |
| maintainer_name | Your name |
| maintainer_xda | https://forum.xda-developers.com/member.php?u=YouID |
| maintainer_country | Country code, eg: BR  |
| xda_thread | XDA thread URL |
| active | true/false |

##### builds/your_device_codename.json
| Param | Description |
|--|--|
| datetime | ... |
| filename | Build file (.zip) name |
| id | Build file (.zip) md5 hash |
| size | Build file (.zip) size (in bytes) |
| url | URL |
| version | 11 |

### Bug report
1. - Before sending bug reports, make sure that the problem is not your tree.
2. - Always send logs!
3. - Reproduce the problem, and if possible with screenshots and screen recording.

### Warnings
Maintainers who fail to comply with these codes of conduct will be alerted 3 times. In case of non-compliance it can be removed from the team without any prior notice.
