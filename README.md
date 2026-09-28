# VeloSearch Studio 🔍

An ultra-fast, modern desktop file search engine for Windows inspired by **Voidtools Everything**, supercharged with real-time multi-format previews, a duplicate file detective, disk storage visualizer, and live batch renamer.

---

## ✨ Features Beyond Everything

- ⚡ **Sub-Millisecond Search**: Real-time search-as-you-type evaluating tens of thousands of files in `< 2 ms`.
- 👁 **Dockable Multi-Format Preview Panel**:
  - **Code & Text**: Syntax highlighted with line counts.
  - **Markdown**: Formatted rich HTML view.
  - **Images**: High-resolution viewer with pixel dimensions.
  - **Hex Viewer**: Raw binary hex dump inspection (Offset, Hex, ASCII).
  - **Folders**: Child item lists and statistics.
- 🔍 **Duplicate File Detective**: 1-click duplicate detection grouping identical files by size and fast xxHash with safe Windows Recycle Bin cleanup.
- 📊 **Storage Visualizer**: Visual breakdown of the largest space-consuming files on your drives with relative percentage bars.
- 🏷️ **Quick Batch Renamer**: Side-by-side live preview batch renamer supporting find & replace, regex, prefixes, suffixes, numbering, and case conversions.
- 🌙 **Modern Dark / Light Theme**: Clean glassmorphic design system using Segoe UI and color-coded file category badges.
- 💾 **Instant Binary Cache**: Starts up in `< 200 ms` on subsequent runs from persistent cache.

---

## 🔎 Search Syntax

| Query | What It Matches |
| :--- | :--- |
| `report` | Files containing "report" in their name |
| `*.py` | All Python source files |
| `ext:pdf,docx` | Files with `.pdf` or `.docx` extensions |
| `size:>100mb` | Files larger than 100 MB |
| `size:<10kb` | Files smaller than 10 KB |
| `type:image` | Images (PNG, JPG, SVG, WebP, etc.) |
| `type:code` | Code files (Python, C++, JS, Rust, etc.) |
| `path:projects` | Files located in any folder named "projects" |
| `dm:today` / `dm:lastday` | Files modified in the last 24 hours |
| `dm:lastweek` / `dm:7d` | Files modified in the past 7 days |
| `dm:lastmonth` / `dm:30d` | Files modified in the past 30 days |
| `dm:lastyear` | Files modified in the past 365 days |
| `dm:>2026-01-01` | Files modified after January 1, 2026 |
| `report size:>10mb ext:pdf dm:lastweek` | Combined search: PDF report over 10 MB modified this week |

---

## 🚀 Simple Mode & Pro Mode

VeloSearch Studio provides two tailored workflows to fit your needs:

1. **⚡ Simple Mode (Default)**:
   - **Ultra-Clean & Minimalist**: Distraction-free instant search bar with a full-width results table.
   - **Maximum Speed**: Perfect for lightning-fast file lookups without visual clutter.
   - **Prominent `[🚀 Pro Mode]` Button**: Switch to Pro Mode with a single click or with `F12`.

2. **🚀 Pro Mode**:
   - **Location Scope & Date Filters**: Filter by specific drives, custom folders, and recently modified timeframes (`Today`, `Yesterday`, `Last Week`, `Last Month`, `Past Year`).
   - **Category Chips & Dynamic Subpills**: 1-click filtering for CAD & 3D, GIS & Geo, Documents (PDF, Word, Excel, PPT, TXT), Code, Images, Audio, Video, Archives, Executables, and Folders.
   - **Deep Content Search**: Search inside PDF, Word `.docx`, Excel `.xlsx`, PPTX, and code files.
   - **1/3 Dockable Live Preview Panel**: Rich document rendering, syntax-highlighted code, image viewer, CAD cards, and hex view.

3. **⚙️ Choose Your Default Startup Mode**:
   - Right-click the `[🚀 Pro Mode]` / `[↩ Simple Mode]` button or open **Tools ▾ > Shortcuts & Startup** to choose whether VeloSearch Studio opens in **Simple Mode** or **Pro Mode** by default.

---

## ⚡ Quick Launcher HUD (Double-Press `Ctrl` or `Ctrl + Space`)
   - **Double-press the `Ctrl` key** (or press `Ctrl + Space` / `Alt + Space`) anywhere in Windows to pop up a sleek, floating, centered Spotlight / PowerToys Run style search bar instantly.
   - **Launch Installed Apps**: Type `calc`, `notepad`, `chrome`, `word`, `excel`, `steam`, etc., and hit `Enter` to run instantly.
   - **Fast File & Folder Finder**: Find documents on the fly, press `Enter` to open or `Ctrl + Enter` to reveal in File Explorer.
   - **Seamless Expansion**: Click the **"Open Studio ↗"** button or hit `Tab` to expand into the full dual-pane search studio with deep content search.
   - **System Tray Mode**: Sits quietly in your system tray with sub-second background readiness so the search bar is always ready.

2. **🖥️ Full Search Studio**:
   - Deep full-text search inside PDFs, Word documents, Excel sheets, and code files.
   - Multi-format preview panel (PDF page renderer, CAD cards, images, markdown, hex).
   - Duplicate file detective, large file storage visualizer, and live batch renamer.

---

## ⌨️ Keyboard Shortcuts

- `Alt + Space` or `Ctrl + Space`: **Toggle Floating Quick Launcher HUD** (from anywhere in Windows)
- `Tab` / `Ctrl + O`: **Open Full Studio** from Quick Launcher HUD
- `F11`: Toggle Live Preview Panel in Full Studio
- `Ctrl + F`: Focus Main Search Bar
- `Ctrl + Shift + F` / `Alt + F`: Focus Two-Stage Content Narrowing Bar
- `F5`: Re-index Drives
- `Enter` / Double Click: Open File / Run App
- `Ctrl + Enter`: Open containing folder in File Explorer
- `Right-Click`: Context menu (Open, Reveal in Explorer, Copy Path, Copy Name, Hash, Search Text Inside Selected, Recycle)

---

## 🚀 Standalone Executables (`.exe`)

VeloSearch Studio is compiled into standalone Windows `.exe` files located in the `dist/` directory:

1. **Portable Application Executable**:
   - Path: `dist/VeloSearchStudio.exe`
   - Single standalone `.exe` that runs immediately without needing Python installed.
   
2. **Windows Setup Installer Wizard (System-Wide & Per-User)**:
   - Path: `dist/VeloSearchStudio_Setup.exe`
   - Setup wizard installer supporting both:
     - 🛡️ **System-Wide Windows Core Installation**: Installs to `C:\Program Files\VeloSearchStudio`, creates shortcuts in Common Desktop (`C:\Users\Public\Desktop`) and All Users Start Menu (`C:\ProgramData\Microsoft\Windows\Start Menu\Programs`), registers in `HKLM` with automatic Windows UAC Administrator elevation.
     - 💡 **Current User Installation**: Installs to `%LOCALAPPDATA%\Programs\VeloSearchStudio` without requiring administrator privileges.
   - Registers Windows Explorer right-click context menu (*"Search with VeloSearch Studio..."*) and optional startup with Windows.

3. **Interactive Search Tutorial**:
   - Built-in multi-step interactive walkthrough dialog to help new users master instant file search, category fine-tuning, in-document deep content search, and subfolder scoping.
   - Launch anytime via `F1` or **Tools ▾ > Search Tutorial & Guide**.

### How to Rebuild the Executables
To recompile the `.exe` binaries from source:
```bash
python build_installer.py
```

### Running from Source
```bash
python main.py
```

### Double-Press Ctrl Quick Search HUD & Global Shortcuts
- **Double-Press `Ctrl`** or **`Ctrl + Space`**: Instant floating Spotlight-style Quick Search HUD anywhere in Windows.
- **`Alt + Space`**: Alternative global shortcut for keyboard accessibility.
- **`Tab` or `Ctrl + O`**: Seamlessly transition from the floating HUD into the full VeloSearch Studio window with your query preserved.

### 📁 Windows Explorer Right-Click Context Menu ("Search with VeloSearch Studio...")
VeloSearch Studio integrates directly into the Windows Shell:
- **Right-Click Any Directory / Folder**: Select *"Search with VeloSearch Studio..."* to launch or focus VeloSearch Studio scoped directly to that folder.
- **Right-Click Open Folder Window Background**: Search within the currently opened folder.
- **Right-Click Any Drive**: Search specifically inside that drive.
- **Single-Instance IPC Forwarding**: If VeloSearch Studio is already open, selecting the context menu communicates via local IPC (`QLocalSocket`) to update the search scope instantly without opening duplicate windows.
- Configure or toggle this integration anytime via the `Windows Quick Access & Startup` menu or during installation.

### Background Startup Reindex (Headless CLI)
VeloSearch Studio supports silent headless indexing:
```bash
# Immediate silent re-index of all drives and save to cache
python main.py --reindex

# Re-index delayed by N seconds (e.g. 180s = 3 min after Windows boot)
python main.py --reindex-delayed 180
```
When enabled in the Windows Integration dialog (`Windows Quick Access & Startup`), Windows automatically triggers this 3 minutes after boot, ensuring that whenever you launch the app, all drives are already freshly pre-indexed!

### ⚡ Rock-Solid Stability Architecture
VeloSearch Studio is built with an enterprise-grade multi-threaded stability model to prevent UI freezes, stuttering, and memory spikes:
- **Asynchronous Preview Worker (`AsyncPreviewWorker` on `QThread`)**: File parsing (PDF rasterization, Excel sheet extraction, Word parsing, CAD DWG/DXF cards) runs in background threads off the Qt GUI thread. Even multi-hundred megabyte files or slow network paths load smoothly without blocking the UI.
- **Debounced Selection Pipeline**: Rapid keyboard arrow-key navigation or mouse wheel scrolling debounces file selection triggers (50ms), preventing disk thrashing and redundant file parsing.
- **Dynamic Worker Cancellation**: Navigating to a new item immediately cancels pending background extraction tasks from previous files, freeing memory and CPU cycles instantly.

                     