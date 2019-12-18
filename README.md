# Oradew VS Code Remote Dev Container

A development container definition with prerequisites (oracle-instantclient, nodejs and git) for Oradew development.

## Prerequisites
- VS Code Extension: Remote - Containers: https://code.visualstudio.com/docs/remote/containers#_getting-started

## Gettin started

1. `git clone https://github.com/mickeypearce/oradew-vscode-container.git` or manually copy the `.devcontainer` directory into your project.
2. Start VS Code and open your project folder.
3. Press <kbd>F1</kbd> and select `Remote-Containers: Reopen Folder in Container` command.
4. Press <kbd>F1</kbd> and select `Oradew: Initialize Workspace/Version` command to start Oradew project.


## Contents

Container consists of Oracle Linux image (oraclelinux:7-slim) with preinstalled:

- oracle-instantclient19.3
- oracle-instantclient19.3-sqlplus
- nodejs-v10.17.0
- git-2.22.0
- Oradew extension
- GitLens extension
- mounts local path "%ORACLE_HOME%/network/admin" (uncomment in devcontainer.json or put your own path)

