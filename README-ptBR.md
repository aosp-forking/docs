# AOSPK - The Kraken Project
## Official devices application

Envie sua solicitação para se juntar à equipe: https://forms.gle/k967Pzrqd1PBSqQTA

Antes de abrir uma solicitação para adicionar seu dispositivo à nossa lista de dispositivos oficiais, você deve saber algumas coisas simples:

### Para se tornar um mantenedor da Kraken:
1. - Você deve ter uma maneira de verificar suas builds, do seu jeito, tendo o dispositivo, ou enviar as builds para alguém testar. Construções às cegas e/ou não testadas não são permitidas.
2. - Você deve ter conhecimento em git.
3. - Você deve fazer uma compilação não oficial e tornar o dispositivo estável para uso diário antes de aplicar.
4. - Você deve ter as fontes do seu dispositivo abertas para nós darmos uma olhada.
5. - Você não deve ser um substituto de outro mantenedor que foi removido. As solicitações consideradas desse tipo não serão aceitas.

### Notas de conduta dos mantenedores:
1. - Os mantenedores devem fazer o upload de suas árvores em [AOSPK-Devices](https://github.com/AOSPK-Devices)
2. - Os mantenedores devem testar cada atualização antes de fazer o upload em nosso OTA.
3. - Os mantenedores devem manter a autoria do Git commits em tudo que eles fizerem uma mudança, mesmo que seja sua árvore de dispositivos, kernel ou fontes de ROM. git commit --amend e force-pushes são aceitáveis.
4. - As divulgações podem ser feitas no PM, Telegram ou XDA.
5. - Os mantenedores também precisam adicionar **export CUSTOM_BUILD_TYPE=OFFICIAL** em seu ambiente de construção para que o aplicativo OTA seja incluído.

### Upload de novas construções:
1. - Certifique-se de que a construção foi testada e está funcionando. Nunca envie uma nova build sem testar!
2. - Faça o upload para nosso host no **SourceForge**. Você pode fazer isso no terminal ou no navegador.
    - Terminal:
    - `scp Kraken-11-20200112-1303-beryllium.zip nomedeusuario@frs.sourceforge.net:/home/frs/p/aospk/seudispositivo`
3. - Para disponibilizá-lo em nosso centro de download é necessário registrar a construção no [AOSPK/official_devices](https://github.com/AOSPK/official_devices).
4. - Somente após essas etapas você estará livre para publicar em canais, grupos e XDA.

### Changelog
Para cada nova versão, você precisa fazer upload do changelog para este repositório na pasta específica do dispositivo.

O nome do arquivo do changelog deve corresponder ao nome do arquivo **.zip** e deve terminar com **.txt**
Ex: **.zip**, **Kraken-11-20200112-1303-beryllium.zip**, o nome do arquivo do changelog deve ser **Kraken-11-20200112-1303-beryllium.txt**

### Over-the-air (OTA) atualizações
Nosso sistema é automático, você não deve se preocupar em atualizar algum script, basta fazer o upload do novo build para o servidor **SourceForge** e enviar uma solicitação com o changelog, e também editar o arquivo JSON do seu dispositivo **builds/device_codename.json**).

Ex: Poco F1 é chamado de **beryllium**, então o arquivo JSON do dispositivo é **builds/beryllium.json**

**Observação:** Novas compilações podem levar até 10 minutos para aparecer no site e no aplicativo OTA.

### JSON parâmetros
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

### Relatório de bug
1. - Antes de enviar relatórios de bug, certifique-se de que o problema não é sua árvore.
2. - Sempre envie logs!
3. - Reproduza o problema e, se possível, com capturas de tela e gravação de tela.

### Alertas
Os mantenedores que não cumprirem esses códigos de conduta serão alertados 3 vezes. Em caso de não conformidade pode ser retirado da equipe sem prévio aviso.
