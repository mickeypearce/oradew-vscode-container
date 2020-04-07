# Oradew VS Code Dev Container

VS Code container definition for Oracle DB development with Oradew.

## Prerequisites

- VS Code Extension: [Remote - Containers](https://code.visualstudio.com/remote-tutorials/containers/getting-started)

## Getting started

1. `git clone https://github.com/mickeypearce/oradew-vscode-container.git` or manually copy the `.devcontainer` directory into your project.
2. Start VS Code and open your project folder.
3. Press <kbd>F1</kbd> and select `Remote-Containers: Reopen Folder in Container` command.
4. Press <kbd>F1</kbd> and select `Oradew: Initialize Workspace/Version` command to start Oradew project.

## Contents

Container consists of Oracle Linux image (oraclelinux:7.7) with preinstalled:

- oracle-instantclient19.3
- oracle-instantclient19.3-sqlplus
- nodejs-v10.17.0
- git-2.22.0
- Oradew extension and `oradew` CLI
- GitLens extension
- Bookmarks extension

## Troubleshooting

Container mounts local path "%ORACLE_HOME%/network/admin" or "%TNS_ADMIN%" to configuration directory inside container (tnsnames.ora, ...). If you don't have ORACLE_HOME or TNS_ADMIN defined on your local system, replace "source" with a full path or remove "mounts" altogether in `devcontainer.json`.

```json
"mounts": [
    "source=${localEnv:ORACLE_HOME}/network/admin,target=/usr/lib/oracle/19.3/client64/lib/network/admin,type=bind,consistency=cached"
]
```


