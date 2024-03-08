# Windows Command Prompt

Getting started with the Windows Command Line (also known as Command Prompt or cmd) for basic file operations involves learning a few essential commands and concepts. The Command Line allows you to perform tasks by typing commands into a text interface, offering a fast and powerful way to interact with your computer. Here's a simple guide to get you started:

### 1. Opening Command Prompt:
- **Search**: Type "cmd" in the Windows search bar and click on the Command Prompt application.
- **Run Dialog**: Press `Win + R`, type "cmd", and press Enter.

### 2. Navigating Directories:
- **View Current Directory**: `cd` (without arguments) shows the current directory.
- **Change Directory**: `cd [directory path]` moves you into the specified directory. Use `cd ..` to move up one level.
- **List Contents**: `dir` displays the contents of the current directory.

### 3. Managing Files and Directories:
- **Creating a Directory**: `mkdir [directory name]` creates a new directory in the current location.
- **Creating a File**: `echo > [file name]` creates a new file. You can also use text editors like Notepad by typing `notepad [file name]`.
- **Renaming Files/Directories**: `ren [original name] [new name]` changes the name of a file or directory.
- **Copying Files**: `copy [source] [destination]` copies files from one location to another.
- **Moving Files**: `move [source] [destination]` moves files from one location to another.
- **Deleting Files**: `del [file name]` deletes a file. Be careful, as this operation is permanent.
- **Deleting Directories**: `rmdir [directory name]` or `rd [directory name]` deletes an empty directory.

### 4. Viewing and Editing Files:
- **Viewing a File**: `type [file name]` displays the contents of a file in the Command Prompt window.
- **Editing a File**: Open files in Notepad for editing with `notepad [file name]`.

### 5. Advanced Commands:
- **Finding Files**: `dir /s /b *.[file extension]` searches for files with a specific extension.
- **File Attributes**: `attrib [file name]` displays or changes file attributes (e.g., read-only, hidden).

### Tips:
- **Autocomplete**: Press `Tab` to autocomplete directory and file names.
- **Command History**: Press `Up` or `Down` arrow keys to scroll through previously used commands.
- **Help**: Typing `[command] /?` provides detailed information about the command's usage.

### Practice:
Try out these commands by performing simple tasks like creating a folder named "Test", navigating into it, creating a text file named "example.txt", and then viewing and editing this file.

As you become more comfortable with these basic commands, you'll find that the Command Prompt is a powerful tool for managing files and directories. Remember to always proceed with caution, especially when using commands that can delete files or directories.
