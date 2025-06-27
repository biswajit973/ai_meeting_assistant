# ImGuiOverlay

A minimal DirectX11 + Win32 overlay using Dear ImGui, designed to be invisible to screen sharing and capture software (e.g., Zoom, Teams, Discord, OBS, etc.) on Windows 10/11.

## Features
- DirectX 11 rendering
- Win32 windowing
- Dear ImGui UI
- Invisible to most screen sharing/capture tools (via `SetWindowDisplayAffinity`)

## Prerequisites
- Windows 10 (version 2004+) or Windows 11
- Visual Studio (2019/2022) or MSVC Build Tools
- C++17 or newer

## Build Instructions

### 1. Clone the Repository
```
git clone https://github.com/yourusername/ImGuiOverlay.git
cd ImGuiOverlay
```

### 2. Open in VS Code (Recommended)
```
code .
```

### 3. Build with MSVC (Visual Studio Build Tools)
- Open the "x64 Native Tools Command Prompt for VS" from the Start Menu.
- Navigate to the project folder:
  ```
  cd path\to\ImGuiOverlay
  ```
- Launch VS Code from this prompt:
  ```
  code .
  ```
- Press `Ctrl+Shift+B` in VS Code to build.

### 4. Run
- Double-click `ImGuiOverlay.exe` or run from the terminal.

## Notes
- The overlay window will **not** appear in most screen sharing/capture software due to the use of `SetWindowDisplayAffinity(hwnd, 0x11)`.
- You can customize the ImGui UI in `main.cpp`.

## Troubleshooting
- If you get `cl.exe not found`, make sure you are using the Developer Command Prompt for Visual Studio.
- If you see linker errors for ImGui symbols, ensure you are using the correct `imgui/backends` source files and headers.
- For Windows 7 or old Windows 10, the capture exclusion may not work.

## Credits
- [ocornut/imgui](https://github.com/ocornut/imgui)

## License
This project is MIT licensed. See `imgui/LICENSE.txt` for Dear ImGui's license.
