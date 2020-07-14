# kotlin

## Installation

```sh
sudo apt install -y zip unzip
curl -s https://get.sdkman.io | bash
source "/home/pydemia/.sdkman/bin/sdkman-init.sh"
sdk install kotlin
```

or

```sh
curl -fsSL https://github.com/JetBrains/kotlin/releases/download/v1.3.72/kotlin-native-linux-1.3.72.tar.gz -O
```


---

AdoptOpenJDK 11

```sh
wget -qO - https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public | sudo apt-key add -
sudo add-apt-repository --yes https://adoptopenjdk.jfrog.io/adoptopenjdk/deb/
sudo apt-get install adoptopenjdk-11-hotspot

export JAVA_HOME="/usr/lib/jvm/adoptopenjdk-11-hotspot-amd64"
sudo ln -sf /usr/bin/java  /usr/lib/jvm/adoptopenjdk-11-hotspot-amd64/bin/java
```


---
VSCode

`.vscode/launch.json` for Debug Tab:
```sh
{
    "configurations": [
        {
            "type": "kotlin",
            "request": "launch",
            "name": "Kotlin Launch",
            "projectRoot": "${workspaceFolder}",
            "mainClass": "com.sk.airuntime.core.BootApplication"
        },
        {
            "type": "kotlin",
            "request": "attach",
            "name": "Kotlin Attach",
            "hostName": "localhost",
            "port": 8000,
            "timeout": 30000
        },
        {
            "type": "java",
            "name": "Spring Boot-BootApplication<ai-runtime-core>",
            "request": "launch",
            "cwd": "${workspaceFolder}",
            "console": "internalConsole",
            "mainClass": "com.sk.airuntime.core.BootApplication",
            "projectName": "ai-runtime-core",
            "args": ""
        }
    ]
}
```
