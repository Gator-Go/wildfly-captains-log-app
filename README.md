# WildFly Booklet App

Prototype. Factory-generated Booklet app from wildfly-builder.

Catalog: https://sw-builder.com/appstore/wildfly/apps/wildfly-captains-log-app.html

Builder: https://github.com/Gator-Go/wildfly-builder

Live demo: https://sw-builder.com/captainsLog/do?op=Home  
Sign in with `guest` / `guest`.

## Build (Unix)

Prerequisites: Git, Groovy, JDK, Maven, WildFly.

Expected sibling directories:

    ~/wildfly/wildfly-builder
    ~/wildfly/wildfly-captains-log-app

```bash
cd ~/wildfly/wildfly-captains-log-app
git pull
./wildfly-captains-log-build-deploy.sh
```
## Layout
```text
wildfly-captains-log-app/
├── wildfly-captains-log-build-deploy.sh
├── Extender/
│   └── BookletExtender.groovy
├── options/                      # app-specific metadata
│   ├── APP_CODE_TYPES.xml
│   ├── APP_ENUMS.xml
│   ├── APP_EVENTS.xml
│   ├── APP_HOME.xml
│   ├── APP_NAMES.xml
│   └── APP_TABLES.xml
├── captainsLog.jpg
├── captainsLog_logo.png
├── cert.jpg
├── SimpleBooklet.jrxml
└── certTest.jrxml
```
## Note:
The template/ and build/ dirs appear after a build. They come from
wildfly-builder.

WildflyBuilder.groovy is copied in from droid-builder at build time.

BookletExtender.groovy performs functions unique to the captainsLog app such as deploying 
the captainsLog logo image.

The captainsLog/ dir appears after a build and is the build output where
the new app is created.



