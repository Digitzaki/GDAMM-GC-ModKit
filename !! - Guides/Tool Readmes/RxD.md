# RxD Hex Editor

~~---------------------------------------------------~~

A modern, professional hex editor designed for clear, efficient binary file modification and analysis. RxD Editor delivers all the essential features of traditional hex editors while introducing enhanced visuals, advanced analysis tools, integrated version control, and workflow-improving productivity features.



## ✨ Features

### Core Editing

~~---------------------------------------------------~~

* **Multi-file tabs** - Open and edit multiple files simultaneously with independent state
* **Smart editing modes** - Insert/overwrite modes with visual indicators
* **Column selection** - Select and edit rectangular regions of bytes
* **Advanced copy/paste** - Multiple formats: Hex, C array, Python bytes, Base64, binary
* **Smart paste** - Configurable delimiter handling for pasting hex strings
* **Full undo/redo** - Complete state snapshots with unlimited history
* **Search \& Replace** - Hex patterns, ASCII strings, UTF-16, regex support
* **Byte operations** - Delete, insert, fill, XOR operations



### Analysis Tools

~~---------------------------------------------------~~

* **Pattern Scanner** - Automatic detection of:

  * ASCII and UTF-16 strings
  * File signatures (PNG, JPEG, ZIP, ELF, PE, etc.)
  * Pointer patterns with validation
  * Compression signatures
* **Data Inspector** - Interpret bytes as 25+ data types:

  * Integers (int8-int64, signed/unsigned)
  * Floats (float32, float64)
  * Timestamps (Unix, Windows FILETIME, DOS)
  * GUIDs, IPv4/IPv6 addresses
  * RGB colors with visual preview
* **Fields System** - Define structured data layouts:

  * Create named fields spanning byte ranges
  * Add nested subfields with type interpretation
  * Auto-generate subfields from pointers
  * Drag-and-drop reordering (subfields locked to parent)
  * Edit values directly with type conversion
* **Statistics \& Visualization**:

  * Byte frequency analysis
  * Entropy calculation
  * Byte distribution graphs
  * Histogram visualization
* **Signature Tracking** - Mark important offsets:

  * Custom labels and data types
  * Inline value display overlays
  * Endianness selection
  * Pointer validation



### Visual Enhancements

~~---------------------------------------------------~~

* **Syntax highlighting** - Color-coded modified/inserted bytes
* **Theme system** - 16+ built-in themes:

  * Dark themes: Dark, Matrix, Nord, Dracula, Monokai, Cyberpunk
  * Light themes: Light, Solarized, GitHub, High Contrast
  * Specialty: Hacker Green, Synthwave, Ocean, Forest, Sunset, Lavender
* **Custom theme editor** - Create themes with:

  * Custom colors for all UI elements
  * Gradient backgrounds (linear, radial, conical)
  * Background image support
  * Save/load custom themes
* **Segment boundaries** - Visual column separators with adjustable ranges
* **Edit box overlay** - Highlight active editing regions
* **Signature overlays** - Inline display of pointer values
* **Configurable display** - 8, 16, 32, or 64 bytes per row



### Productivity Tools

~~---------------------------------------------------~~

* **Notes System** - Attach notes to byte ranges:

  * Rich text formatting
  * Color-coded categories
  * Search and filter notes
  * Quick navigation
* **Version Control** - Built-in snapshot system:

  * Automatic snapshots on edits
  * Manual snapshots with descriptions
  * Browse and restore previous versions
  * Compare snapshots
* **Bookmarks** - Quick navigation to important offsets
* **File Comparison** - Side-by-side file diff view
* **Debugging Console** - Real-time terminal output viewer:

  * Copy and clear functionality
  * Auto-scrolling
  * Theme-styled interface
* **Relative Offset Display** - Show offsets relative to selection or cursor
* **Hidden Delimiters** - Hide specific byte values as spacing



### File Operations

~~---------------------------------------------------~~

* **Large file support** - Memory-mapped I/O for files over 100MB
* **Import/Export** - Export selected regions to new files
* **Multiple file formats** - Import from hex strings, C arrays, Python bytes
* **File metadata** - View creation/modification dates, calculate MD5/SHA256 hashes
* **Recent files** - Quick access to recently opened files
* **Auto-save** - Configurable auto-save with snapshots



## 🚀 What's New in This Release

~~---------------------------------------------------~~

This release introduces major enhancements:



* **Fields system** - Structure your data with nested fields and type interpretation
* **Enhanced pointer system** - Auto-generate subfields from pointers in fields
* **Debugging console** - Monitor and copy terminal output
* **Improved drag-and-drop** - Subfields stay within their parent fields
* **Theme improvements** - Enhanced custom theme editor
* **Stability improvements** - Bug fixes and performance optimizations



## Interface Overview

~~---------------------------------------------------~~

### Menu Bar

~~---------------------------------------------------~~

**File Menu**

~~---------------------------------------------------~~

* Open, Close, Close All - Manage files in tabs
* Save, Save All - Save modifications
* Exit



**Edit Menu**

~~---------------------------------------------------~~

* Undo/Redo - Full undo/redo support
* Copy, Cut, Paste Write, Paste Insert - Advanced clipboard operations
* Fill Selection - Fill selected bytes with a pattern



**View Menu**

~~---------------------------------------------------~~

* Search, Replace, Go to - Navigation and search tools
* Hide Delimiters - Configure bytes to hide with padding
* Segments - Configure visual byte grouping separators



**Tools Menu**

~~---------------------------------------------------~~

* Highlight - Create custom byte pattern highlights
* Show Notes - Open persistent notes panel
* Calculator - Built-in programmer's calculator
* Color Picker - RGB/Hex color picker tool
* Compare Data - Compare bytes between files or regions



**Options Menu**

~~---------------------------------------------------~~

* Version Control - Manage file snapshots and restore points
* Themes - Select from built-in themes or create custom ones
* Save/Load JSON - Export/import highlights and annotations
* Clear - Remove all highlights and annotations



### Main Display

~~---------------------------------------------------~~

**Three-Column Layout:**

* **Offset Column** (left) - Byte positions (click header to cycle: hex/decimal/octal)
* **Hex Column** (center) - Hexadecimal byte values with editing support
* **Decoded Text** (right) - ASCII representation with extended character support



**Features:**

~~---------------------------------------------------~~

* Click any byte to position cursor
* Type hex digits to edit bytes directly
* Right-click for context menu
* Multi-file tabs for working with multiple files
* Column selection mode for rectangular selections



### Right Panel Tabs

~~---------------------------------------------------~~

**Inspector Tab**

~~---------------------------------------------------~~

* View selected bytes as different data types
* Signed/unsigned integers (8, 16, 32, 64-bit)
* Floating point (float, double)
* Text encodings (ASCII, UTF-8, UTF-16)
* Binary representation
* Toggle byte order (little/big endian)
* Choose integral display basis (hex/dec/oct)
* Navigation buttons (first, prev, next, last byte)



**Pattern Scan Tab**

~~---------------------------------------------------~~

* Automatic pattern detection in files
* Identifies ASCII strings, UTF-16LE strings
* Detects pointer tables and possible file offsets
* Finds compression signatures (zlib, gzip, LZ4, etc.)
* Discovers image format headers
* Uses libmagic for MIME type detection
* Click results to jump to location



**Pointers Tab**

~~---------------------------------------------------~~

* Manage custom data signatures and pointers
* Define data structures with types and labels
* Visual overlays show pointer target values
* Organize with categories
* Save/load pointer definitions



**Statistics Tab**

~~---------------------------------------------------~~

* Real-time file statistics
* Byte frequency analysis
* Byte distribution histogram
* Entropy calculation
* Magic number detection
* Visual charts (requires matplotlib)



### Status Bar

~~---------------------------------------------------~~

Shows current file state:

* Cursor position and selected byte range
* File size and modification status
* Ready state indicator



## Key Features

~~---------------------------------------------------~~

**Multi-Tab Editing** - Work with multiple files simultaneously

**Version Control** - Create snapshots and restore to previous states

**Custom Themes** - 25+ built-in themes (dark, light, gradient) plus custom theme editor

**Advanced Selection** - Standard and column selection modes for precise byte operations

**Pattern Highlighting** - Define and colorize byte patterns with labels and categories

**Notes System** - Persistent notes that save with your workflow

**Delimiter Hiding** - Hide repeated delimiters (like null bytes) with padding indicators

**Segment Separators** - Visual grouping of bytes (1, 2, 4, or 8 byte segments)

**Memory Mapped Files** - Efficient handling of large files (10MB+)

**Smart Resolution Detection** - Automatically adjusts UI based on screen resolution (1080p/1440p+)



## Keyboard Shortcuts

~~---------------------------------------------------~~

* **Ctrl+S** - Save file
* **Ctrl+Shift+S** - Save all files
* **Ctrl+Z** - Undo
* **Ctrl+Y** - Redo
* **Ctrl+C** - Copy selection
* **Ctrl+X** - Cut selection
* **Ctrl+V** - Paste insert
* **Ctrl+B** - Paste write (overwrite)
* **Ctrl+F** - Search
* **Ctrl+R** - Replace
* **Ctrl+G** - Go to offset
* **Ctrl+H** - Highlight dialog
* **Ctrl+L** - Fill selection
* **Arrow Keys** - Navigate bytes



## Quick Start

1. **Open a file** - File → Open or drag and drop
2. **Navigate** - Click bytes or use arrow keys
3. **Edit** - Type hex digits directly or use ASCII column
4. **Inspect** - Right panel Inspector shows selected bytes as different data types
5. **Scan** - Use Pattern Scan tab to analyze file structure
6. **Highlight** - Mark important bytes with custom colors and labels (Ctrl+H)
7. **Save** - Ctrl+S to save changes



