# VeloSearch Studio — Release v1.4.0

### What's New in v1.4.0 🚀
- **System-Wide Windows Core Installer**: Setup wizard supports 1-click machine-level core Windows installation into `C:\Program Files\VeloSearchStudio`, Public Desktop, All Users Start Menu, and `HKLM` registry with automatic UAC Administrator elevation. Also retains current-user per-user installation.
- **Interactive Search Tutorial**: Built-in 4-step interactive guide dialog (`F1` or **Tools > Search Tutorial & Guide**) with hands-on practice sandbox for instant search, category narrowing, full-text content search, and subfolder scoping.
- **Streamlined Filter Bar Layout**: Swapped "📁 In Subfolder" and "📄 Search Inside Content" bars for a natural visual hierarchy and smoother workflow.
- **Online Auto-Updater**: Instant GitHub Releases checking, live update changelog display, direct installer downloading with live progress bar, and 1-click seamless installation.
- **Popularity & Usage Metrics**: Built-in privacy-first, completely anonymous ping to measure active installation counts and user engagement.
- **GitHub Release Package**: Fully organized release folder with `VeloSearchStudio.exe` (portable), `VeloSearchStudio_Setup.exe` (Windows Installer), and backup zip archives.
- **Automated CI/CD**: Complete `.github/workflows/build-release.yml` GitHub Actions pipeline for compiling Windows binaries on release tags.
- **Sub-Millisecond Search-as-you-Type**: Multi-threaded index with background cache loader so the UI starts instantaneously.
- **Deep Full-Text Content Search**: Search inside PDF, Word, Excel, PowerPoint, Text, and CAD files with keyword snippet highlighting.
- **Double-Ctrl Quick Launcher HUD**: Instant Spotlight-like HUD launcher across any Windows application.
- **Windows Shell Integration**: Right-click any folder or drive in Windows Explorer to open VeloSearch Studio scoped directly to that folder.

### Downloads:
- **Installer (Recommended)**: `VeloSearchStudio_Setup.exe` (System-Wide or Per-User installer with Desktop icon, Start Menu shortcut, and Explorer Context Menu)
- **Portable**: `VeloSearchStudio.exe` (Single standalone executable, zero installation required)
- **ZIP Bundle**: `VeloSearchStudio-v1.4.0.zip` (Contains both binaries)

*Crafted by Ranjan*
