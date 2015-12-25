Apache Cordova
==============

Command-Line Shortcuts
----------------------

**Creating projects**
```bash
# Creates a project:
# cordova create <project> <reverse-domain> <ClassName>
cordova create test com.my_domain.test Test
```

**Adding and listing platforms**
```bash
# Adds an specific platform:
# cordova platform add <platform>
cordova platform add android

# List installed and available platforms
cordova platform ls
```

**Compiling platforms**
```bash
# Builds a platform:
# cordova build [<platform>]
cordova build android
```

The previous command is equivalent to
```bash
# copies files and compiles the sources
cordova prepare android
cordova compile android
```
