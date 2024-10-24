# Mac Terminal Cheat Sheet

## 1. **Navigation**

### `cd` - Change Directory
Change the current working directory.

- **Command**:
  ```bash
  cd /path/to/directory
  ```
- **Examples**:
  ```bash
  cd ~/Documents        # Go to the Documents folder in your home directory
  cd /usr/local/bin     # Go to a system folder
  ```

### `pwd` - Print Working Directory
Displays the current working directory.

- **Command**:
  ```bash
  pwd
  ```
- **Example**:
  ```bash
  /Users/username/Projects # Output showing current location
  ```

### `ls` - List Directory Contents
List files and folders in the current or specified directory.

- **Commands**:
  ```bash
  ls            # List all files in the current directory
  ls -la        # List all files including hidden, with detailed information
  ```
- **Examples**:
  ```bash
  ls ~/Desktop  # List contents of Desktop folder
  ls -l /etc    # List contents of /etc with detailed view
  ```

## 2. **File Operations**

### `touch` - Create an Empty File
Creates a new empty file.

- **Command**:
  ```bash
  touch filename
  ```
- **Example**:
  ```bash
  touch newfile.txt  # Create a new file called 'newfile.txt'
  ```

### `mkdir` - Make Directory
Creates a new directory.

- **Command**:
  ```bash
  mkdir dirname
  ```
- **Example**:
  ```bash
  mkdir my_folder     # Create a new folder called 'my_folder'
  ```

### `rm` - Remove Files or Directories
Delete a file or directory.

- **Commands**:
  ```bash
  rm filename          # Remove a file
  rm -r directoryname  # Remove a directory and its contents
  ```
- **Examples**:
  ```bash
  rm oldfile.txt       # Delete 'oldfile.txt'
  rm -r my_folder      # Delete 'my_folder' and its contents
  ```

### `cp` - Copy Files or Directories
Copy files or directories from one place to another.

- **Commands**:
  ```bash
  cp source destination       # Copy a file
  cp -r source_directory destination_directory  # Copy a directory
  ```
- **Examples**:
  ```bash
  cp file.txt /backup/file.txt   # Copy 'file.txt' to the backup folder
  cp -r ~/Documents ~/Backup     # Copy Documents folder to Backup
  ```

### `mv` - Move Files or Directories
Move or rename files or directories.

- **Commands**:
  ```bash
  mv source destination       # Move a file or directory
  mv oldname newname          # Rename a file or directory
  ```
- **Examples**:
  ```bash
  mv report.docx /Documents/   # Move 'report.docx' to Documents
  mv oldname.txt newname.txt   # Rename 'oldname.txt' to 'newname.txt'
  ```

## 3. **Viewing & Editing Files**

### `cat` - Concatenate and Display File Content
Displays the content of a file.

- **Command**:
  ```bash
  cat filename
  ```
- **Example**:
  ```bash
  cat notes.txt  # Display contents of 'notes.txt'
  ```

### `nano` - Edit File with Nano Text Editor
Opens a file in the Nano text editor.

- **Command**:
  ```bash
  nano filename
  ```
- **Example**:
  ```bash
  nano todo.txt  # Open 'todo.txt' for editing
  ```

### `less` - View File Content Page by Page
View the content of a file one page at a time.

- **Command**:
  ```bash
  less filename
  ```
- **Example**:
  ```bash
  less longfile.txt  # View 'longfile.txt' one page at a time
  ```

## 4. **Search**

### `find` - Search for Files
Find files or directories in a specified location.

- **Command**:
  ```bash
  find /path -name filename
  ```
- **Example**:
  ```bash
  find ~/Documents -name "*.pdf"  # Find all PDFs in the Documents folder
  ```

### `grep` - Search Inside Files
Search for a text pattern inside files.

- **Command**:
  ```bash
  grep "pattern" filename
  ```
- **Example**:
  ```bash
  grep "error" log.txt  # Find all lines with 'error' in 'log.txt'
  ```

## 5. **System Info & Utilities**

### `top` - View Running Processes
Display system tasks and resource usage.

- **Command**:
  ```bash
  top
  ```
- **Example**:
  ```bash
  top  # View active processes and resource usage
  ```

### `df` - Disk Usage
Displays disk space usage of file systems.

- **Command**:
  ```bash
  df -h
  ```
- **Example**:
  ```bash
  df -h  # View disk usage in a human-readable format
  ```

### `du` - Directory Space Usage
Displays disk usage of directories and files.

- **Command**:
  ```bash
  du -h /path/to/directory
  ```
- **Example**:
  ```bash
  du -h ~/Downloads  # View size of each item in Downloads folder
  ```

## 6. **Networking**

### `ping` - Test Network Connection
Send ICMP ECHO_REQUEST to a network host.

- **Command**:
  ```bash
  ping hostname
  ```
- **Example**:
  ```bash
  ping google.com  # Test connection to Google
  ```

### `curl` - Transfer Data from/to a Server
Fetch content from a URL.

- **Command**:
  ```bash
  curl url
  ```
- **Example**:
  ```bash
  curl https://example.com  # Fetch HTML of example.com
  ```

## 7. **Permissions**

### `chmod` - Change File Permissions
Modify file permissions.

- **Command**:
  ```bash
  chmod permissions filename
  ```
- **Example**:
  ```bash
  chmod 755 script.sh  # Set executable permissions for 'script.sh'
  ```

### `chown` - Change File Owner
Change the owner of a file or directory.

- **Command**:
  ```bash
  chown user:group filename
  ```
- **Example**:
  ```bash
  chown username:staff myfile.txt  # Change owner to 'username' and group to 'staff'
  ```

## 8. **Compression**

### `zip` - Compress Files
Compress files into a ZIP archive.

- **Command**:
  ```bash
  zip archive.zip filename1 filename2
  ```
- **Example**:
  ```bash
  zip backup.zip file1.txt file2.txt  # Create 'backup.zip' containing 'file1.txt' and 'file2.txt'
  ```

### `unzip` - Extract ZIP Archives
Extract files from a ZIP archive.

- **Command**:
  ```bash
  unzip archive.zip
  ```
- **Example**:
  ```bash
  unzip backup.zip  # Extract files from 'backup.zip'
  ```

---

Feel free to use this cheat sheet as a quick reference to get familiar with the most common Mac terminal commands! Practice using these commands to make the terminal feel more intuitive.
