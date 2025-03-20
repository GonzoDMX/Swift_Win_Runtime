# Swift on Windows: Setup Guide

## Automated Setup

1. Install [Docker Desktop](https://www.docker.com/products/docker-desktop/)
2. Install [Visual Studio Code](https://code.visualstudio.com/)
3. Clone this repository
4. Right-click `setup.ps1` and select "Run with PowerShell"
5. When VS Code opens, click "Reopen in Container" when prompted
6. Wait for container build to complete

## Manual Setup

### Required Software
1. Install [Docker Desktop](https://www.docker.com/products/docker-desktop/)
2. Install [Visual Studio Code](https://code.visualstudio.com/)
3. Install VS Code extensions:
   - Dev Containers -> https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers
   - Swift (swiftlang.swift-vscode) -> https://marketplace.visualstudio.com/items?itemName=swiftlang.swift-vscode
   - CodeLLDB (vadimcn.vscode-lldb) -> https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb

### Setup Steps
1. Clone this repository
2. Start Docker Desktop
3. Open VS Code
4. File > Open Folder > Select the cloned repository
5. When prompted, click "Reopen in Container" (or press F1, type "Remote-Containers: Reopen in Container")
6. Wait for container build to complete (5-10 minutes first time)

## Verifying Installation
1. Open the Examples/BasicSyntax/01_HelloWorld.swift file
2. Press Ctrl+Shift+B to run it
3. You should see "Hello, World!" in the terminal

## Running Swift Code

### Single Files
1. Open a .swift file
2. Press Ctrl+Shift+B or select the "Run Current Swift File" task

### Swift Packages
1. Navigate to a directory with Package.swift
2. Use "Swift Package: Build" task to build
3. Use "Swift Package: Run" task to run

## Troubleshooting
1. If Docker isn't starting, restart your computer
2. If container fails to build, check internet connection
3. If VS Code extensions aren't loading, try reinstalling them
4. For Swift command errors, ensure the container is fully built

## Additional Resources
1. [Swift Language Guide](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/thebasics/)
2. [VS Code Remote Containers Documentation](https://code.visualstudio.com/docs/remote/containers)
