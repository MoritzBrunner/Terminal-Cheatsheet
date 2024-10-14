# Mac Terminal Cheatsheet

## 1. Navigating the File System
- `ls` : List files and directories
- `cd [path]` : Change directory
- `pwd` : Show current directory path
- `mkdir [directory_name]` : Create a new directory
- `rmdir [directory_name]` : Remove an empty directory

## 2. Managing Files
- `touch [filename]` : Create a new empty file
- `cp [source] [destination]` : Copy file
- `mv [source] [destination]` : Move or rename a file
- `rm [filename]` : Delete a file
- `rm -r [directory_name]` : Delete a directory and its contents

## 3. Viewing and Editing Files
- `cat [filename]` : Show file content
- `less [filename]` : View file content page by page
- `head -n [number] [filename]` : Display the first `n` lines of a file
- `tail -n [number] [filename]` : Display the last `n` lines of a file
- `nano [filename]` : Edit file with Nano editor
- `vim [filename]` : Edit file with Vim editor (advanced)

## 4. File Permissions
- `ls -l` : List files with permissions
- `chmod [permissions] [filename]` : Change file permissions (e.g., `chmod 755 script.sh`)
- `chown [user]:[group] [filename]` : Change file owner

## 5. System Monitoring and Process Control
- `ps` : Display currently running processes
- `top` : Show system resource usage in real time
- `kill [PID]` : Terminate a process by its PID
- `killall [process_name]` : Terminate all processes by name

## 6. Networking Commands
- `ping [URL or IP]` : Check if a host is reachable
- `ifconfig` : Show network interfaces and IP addresses
- `curl [URL]` : Send HTTP request (for downloads or API calls)
- `ssh user@host` : Connect to a remote server via SSH

## 7. Homebrew Package Manager (if installed)
- `brew install [package_name]` : Install a package
- `brew update` : Update Homebrew and installed packages
- `brew list` : List installed packages
- `brew uninstall [package_name]` : Uninstall a package

## 8. Useful Keyboard Shortcuts
- `Ctrl + C` : Cancel the current command
- `Ctrl + D` : Close the terminal session
- `Ctrl + U` : Clear the current line
- `Tab` : Autocomplete command or file name
- `↑/↓` : Scroll through command history

## 9. Useful Tools
- `find [path] -name [filename]` : Search for a file by name
- `grep [pattern] [filename]` : Search for text patterns in a file
- `command1 | command2` : Use the output of `command1` as input for `command2` (pipe)
  
## 10. Debugging and Troubleshooting
- `command > output.txt 2>&1` : Redirect command output and errors to a file
- `sudo [command]` : Execute a command with superuser privileges (use with caution)
  
## 11. Additional Resources
- [Mac Terminal Documentation](https://ss64.com/osx/)
- [Homebrew Documentation](https://brew.sh/)
