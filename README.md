
# Universal Installer Config (.uic) for VS Code

This extension provides first-class support for the **Universal Installer Project** configuration files. It transforms standard text editing into a specialized development environment for building installers by adding custom syntax highlighting and intelligent code snippets tailored to the `.uic` format.

## Features

### 🎨 Custom Syntax Highlighting

Unlike standard INI highlighters, this extension recognizes the specific architectural blocks of the Universal Installer:

-   **Core Sections:** Distinct coloring for `[Setup]`, `[Files]`, `[Registry]`, `[Icons]`, and more.
    
-   **Constants:** Highlights built-in path constants like `{app}`, `{pf}`, and `{tmp}`.
    
-   **Booleans & Keys:** Specialized highlighting for installer-specific keys (e.g., `AppName`, `Compression`) and their values.
    

### 💡 Intelligent Snippets

Accelerate your workflow with boilerplate templates for common installer tasks:

-   **`[Setup]` Block:** Quickly generate a full application configuration including versioning and publisher details.
    
-   **`file` Entry:** Add new files with pre-defined flags like `ignoreversion` and `recurse`.
    
-   **`reg` Entry:** Create registry keys with dropdown choices for `Root` types (HKLM, HKCU, etc.).
    

## Getting Started

1.  Create a new file or rename an existing configuration to end in `.uic` (e.g., `install-config.uic`).
    
2.  Open the file in VS Code.
    
3.  The language mode should automatically switch to **Universal Installer Config**.
    
4.  Start typing `[` or `file` to see the intelligent suggestions in action.
    

## Requirements

This extension is designed to work with the **Universal Installer Project** core engine. Ensure your compiler and wizard executables are updated to recognize the `.uic` extension.

## Extension Settings

This extension contributes the following settings:

-   `uic.enableSnippets`: Enable/disable the custom installer code snippets (Default: `true`).
    
-   `uic.formatOnSave`: (Optional) Automatically cleans up whitespace in your `.uic` files.
    

## Known Issues

-   **Punycode Warnings:** You may see a deprecation warning in the extension host logs if using older versions of VS Code; this is a platform-level notice and does not affect extension performance.
    
-   **Large Files:** Very large configuration files (>5000 lines) may experience slight syntax highlighting latency.
    

## Release Notes

### 1.0.0

-   Initial release with support for `.uic` syntax highlighting.
    
-   Added snippets for `Setup`, `Files`, `Dirs`, and `Registry` sections.
    
-   Integrated path constant recognition.

### 20.25.12.1

-   Updated Versioning
-   Added Repo to the package.json
    

----------

**[Universal Installer Project on GitHub](https://www.google.com/search?q=https://github.com/michaelmadell/universalinstaller)**