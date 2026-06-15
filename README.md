<div align="center">
  <p>
    <a href="README.md">🇬🇧 English</a> | <a href="README_tr.md">🇹🇷 Türkçe</a>
  </p>
  <h1>💎 KristalBASIC</h1>
  <p><strong>A modern programming language combining C's performance with BASIC's syntax simplicity.</strong></p>

  [![License: Freeware](https://img.shields.io/badge/License-Freeware-blue.svg)](#license)
  [![Platform: Windows](https://img.shields.io/badge/Platform-Windows%20x64-lightgrey.svg)](#)
  [![VS Code Extension](https://img.shields.io/badge/VS%20Code-Extension%20Available-blue)](#)
</div>

---

## 🌟 What is it?

**KristalBASIC** is an independent programming language that uses the powerful **GCC (MinGW-w64)** backend to compile your code directly into native Windows applications (`.exe`). 

Without wrestling with the steep learning curve of C/C++, you can develop high-performance desktop software and 3D games using the highly readable and easy-to-write BASIC syntax.

## ✨ Key Features

*   🚀 **C-Level Performance:** Your code is not interpreted; it is compiled directly to native machine code.
*   🎮 **Built-in 3D Game Engine:** The world-renowned [Raylib](https://www.raylib.com/) library is embedded within the compiler. You can instantly manage 2D/3D graphics, physics, audio, and input without any extra setup.
*   📦 **Zero Dependencies:** The `.exe` files you generate run on any Windows PC without requiring additional DLLs or runtime libraries.
*   🛠️ **VS Code Integration:** Offers autocomplete (IntelliSense) and syntax highlighting via the official VSIX extension for Visual Studio Code.

## 📥 Installation

1.  Navigate to the **[Releases](../../releases)** tab and download the latest `KristalBASIC_Setup.exe`.
2.  Run the setup to install the compiler on your system.
3.  Download the `kristalbasic-vscode.vsix` file from the Releases section.
4.  Open VS Code, go to the **Extensions** tab, click the `...` menu on the top right, select **"Install from VSIX..."**, and install the extension.

## 💻 Quick Start (Code Snippet)

Open Visual Studio Code, create a `.kbas` file, and type the following code:

```basic
' First window with KristalBASIC!
Include "raylib"

InitWindow 800, 450, "KristalBASIC - Hello World"
SetTargetFPS 60

While Not WindowShouldClose()
    BeginDrawing()
        ClearBackground RAYWHITE
        DrawText "Welcome to the KristalBASIC 3D World!", 190, 200, 20, LIGHTGRAY
    EndDrawing()
Wend

CloseWindow()
```

## 🎮 Example 3D Game

To see the capabilities of KristalBASIC in action, check out the **Example 3D Game** in the provided `Examples` folder or manuals. This demonstrates how to load 3D models, manage camera controls, and handle collision tests hands-on.

## 📄 License (Freeware)

*   **Compiler and Tools:** The KristalBASIC compiler is closed-source and entirely **Freeware**. 
*   **Your Applications:** All applications, games, and software you develop using KristalBASIC are **100% YOURS**. You can distribute your apps as open-source or sell them commercially. Your projects are not restricted by GCC or Raylib licenses (No GPL restrictions apply to your binaries).
*   **Example Codes:** All example source codes provided are under the **MIT License**, free to use and modify in your own projects.

For more details, please see the license file in the root directory.

---
<div align="center">
  Developed with ❤️ by <b>Kristalsoft</b> in Türkiye. 🇹🇷
</div>
