# AutoSort

AutoSort is a lightweight Python CLI utility that automatically organizes files in the current directory based on their file type.

Instead of manually sorting downloads, project folders, or messy directories, AutoSort reads a configuration file and moves files into categorized folders such as Images, Documents, Video, Code, Archives, and more.

It is designed to be simple, customizable, and easy to run from any directory.

---

## Features

* Automatically sorts files by extension
* Works in the **current directory**
* Fully **configurable file categories**
* Lightweight with **no external dependencies**
* Simple **CLI command usage**
* Works great on **Linux environments**

---

## How It Works

AutoSort reads a configuration file (`config.json`) that maps file extensions to folder names.

Example:

```json
{
  "Images": ["jpg", "png", "jpeg"],
  "Documents": ["pdf", "docx", "txt"],
  "Audio": ["mp3"],
  "Code": ["py", "js", "cpp"]
}
```

When you run the command, files are automatically moved into folders based on their extension.

Example directory before running AutoSort:

```
Downloads/
 ├── photo.jpg
 ├── report.pdf
 ├── music.mp3
 ├── script.py
```

After running AutoSort:

```
Downloads/
 ├── Images/
 │   └── photo.jpg
 ├── Documents/
 │   └── report.pdf
 ├── Audio/
 │   └── music.mp3
 └── Code/
     └── script.py
```

---

# Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/AutoSort.git
cd AutoSort
```

---

### 2. Move the script to your local binaries

```bash
mkdir -p ~/.local/bin
mv autosort ~/.local/bin/
chmod +x ~/.local/bin/autosort
```

---

### 3. Ensure `~/.local/bin` is in your PATH

Check with:

```bash
echo $PATH
```

If it is not present, add this line to your shell config:

**For bash**

```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

**For zsh**

```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

---

# Configuration

Edit the `config.json` file to customize file categories and extensions.

Example structure:

```json
{
  "Images": ["jpg", "jpeg", "png"],
  "Documents": ["pdf", "doc", "docx"],
  "Audio": ["mp3", "wav"],
  "Video": ["mp4", "mkv"],
  "Code": ["py", "js", "cpp"]
}
```

You can add or remove categories depending on your needs.

---

# Usage

Navigate to any directory you want to organize and run:

```bash
autosort
```

AutoSort will automatically create folders (if they don't exist) and move files accordingly.

---

# Requirements

* Python 3.x
* Linux / Unix-like environment

(No external Python libraries required)

---

# Future Improvements

* Ignore already sorted folders
* CLI arguments for custom directories
* Logging support
* Dry-run mode
* Installable pip package

---

# Contributing

Pull requests and suggestions are welcome. Feel free to open an issue if you find bugs or have ideas for improvements.

---

# License

MIT License
