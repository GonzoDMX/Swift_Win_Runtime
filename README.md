# Swift Development on Windows

This repository contains a pre-configured Swift development environment for Windows users. It uses Visual Studio Code and Docker to provide a consistent, easy-to-use environment for learning Swift programming without needing a Mac.

## Getting Started

### Prerequisites

- Windows 10/11 with virtualization enabled
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Visual Studio Code](https://code.visualstudio.com/)
- Git

### Quick Setup (Recommended)

1. **Clone this repository:**
   ```
   git clone https://github.com/your-username/swift-course-windows.git
   cd swift-course-windows
   ```

2. **Run the automated setup script:**
   - Right-click `setup.ps1` and select "Run with PowerShell"
   - The script will check for and install required software
   - Follow any on-screen prompts

3. **Start coding:**
   - VS Code will open automatically
   - When prompted, click "Reopen in Container"
   - Wait for the container to build (first time only, may take 5-10 minutes)
   - You're ready to write Swift code!

### Manual Setup

If the automated script doesn't work for your system:

1. **Install required software:**
   - Install [Docker Desktop](https://www.docker.com/products/docker-desktop/)
   - Install [Visual Studio Code](https://code.visualstudio.com/)
   - Install required VS Code extensions:
     - Remote - Containers
     - Swift
     - CodeLLDB

2. **Clone this repository:**
   ```
   git clone https://github.com/your-username/swift-course-windows.git
   cd swift-course-windows
   ```

3. **Open in VS Code and start the container:**
   - Open VS Code
   - File > Open Folder > Select the cloned repository
   - When prompted, click "Reopen in Container"
   - Alternatively, press F1, type "Remote-Containers: Reopen in Container" and select it

## Course Materials

This repository is organized as follows:

- **Examples**: Sample Swift code demonstrating key concepts
  - **BasicSyntax**: Fundamental Swift language features
  - **OOP**: Object-oriented programming examples
  - **SimplePackage**: Basic Swift package structure
  - **ConsoleApp**: Command-line application example

- **Assignments**: Starter code for course assignments
  - Each assignment includes a README with requirements

- **Resources**: Additional reference materials
  - Swift syntax cheat sheet
  - Style guide
  - Troubleshooting common issues

## Working with Swift

### Running Swift Code

#### Single Swift Files

To run a single Swift file:
1. Open the Swift file in VS Code
2. Press Ctrl+Shift+B or use the "Run Current Swift File" task

#### Swift Packages

For Swift package projects:
1. Navigate to a directory with a Package.swift file
2. Use the "Swift Package: Build" and "Swift Package: Run" tasks

### Keyboard Shortcuts

- **Ctrl+Shift+B**: Run the current Swift file
- **F5**: Debug the current file/package (requires compilation first)
- **Ctrl+Shift+P**: Open Command Palette for more options

## Container Features

The Swift development container includes:

- Swift 5.9 toolchain
- LLDB debugger
- SourceKit-LSP for code navigation
- Git for version control
- Node.js for web development

## Assignments

The assignments follow this general structure:

1. **Assignment 1**: Basic Swift syntax and control flow
2. **Assignment 2**: Functions, collections, and optionals
3. **Assignment 3**: Object-oriented programming concepts
4. **Final Project**: Comprehensive Swift application

Each assignment folder contains a README with specific requirements and starter code.

## Troubleshooting

### Container Fails to Build

- Make sure Docker Desktop is running
- Try restarting Docker Desktop
- Check that you have a stable internet connection

### Swift Commands Not Found

- Make sure the container has finished building
- Check that you're running commands in the integrated terminal
- Try reopening VS Code and the container

### VS Code Extensions Not Working

- Make sure you're connected to the development container
- Check the Extensions panel to see which extensions are enabled

### Need More Help?

- Check the Resources/CommonIssues.md file
- Post in the course forum
- Email the instructor or teaching assistant

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- [Swift.org](https://swift.org/) for the Swift language and toolchain
- [Microsoft](https://code.visualstudio.com/) for Visual Studio Code
- [Docker](https://www.docker.com/) for containerization technology
