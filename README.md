Apache Cordova
==============

Command-Line Shortcuts
----------------------

**Getting help**
```bash
# Prints general help
cordova --help

# Prints command help:
# cordova <command> --help
cordova create --help
```

**Creating projects**
```bash
# Creates a project:
# cordova create <project> <reverse-domain> <ClassName>
cordova create my-first-app com.my_domain.my_first_app MyFirstApp
```

The argument `reverse-domain` does not accept hyphen characters (-).

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

**Running platforms**
```bash
# Runs an specific platform:
# cordova run <platform>
cordova run android
```

The previous command is equivalent to
```bash
# copies files and compiles the sources
cordova prepare android
cordova compile android
```
