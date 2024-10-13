# Terminal-Cheatsheet
A comprehensive Cheatsheet containing the Basics of the Mac Terminal

| Symbol | Meaning |
|:----:|----|
| **%** | Terminal Command |
| ⌨️ | Keyboard Shortcut |
| 💡 | Aditional Information |


## File Manipulation

| Operation | Usage | Name |Description |
| :---: | :---------- | :--- | :--- |
| `>>` | `[Command]`&nbsp;`>>`&nbsp;`[/File]` | Append Output Redirection[^Example] | Append the output of the Command to the File. Creates a new File if the specified File does not jet exist. |
| `>` | `[Command]`&nbsp;`>`&nbsp;`[/File]` | Override, Output Redirection | Override the File with the output of the Command. Creates a new File if the specified File does not jet exist. |

Operation | Description |
| :--- | :--- |
| `echo`&nbsp;`"Your Text"`&nbsp;`>>`&nbsp;`[/File]` | Append Your Text to the File. |
| `cat`&nbsp;`[/FileA]`&nbsp;`>>`&nbsp;`[/FileB]` | Append the contents of a FileA to FileB. |

| Operation | Name | Description |
| :---: | :--- | :--- |
| `>>` | Append Output Redirection | Append the output of the Command to the File. Creates a new File if the specified File does not jet exits.
| `>` |  Override, Output Redirection | Override the File with the output of the Command. Creates a new File if the specified File does not jet exits.|

[^Example]: `echo "some text" >> myFile.txt`

| Operation | Usage | Name | Description 
| :---: | :---------- | :--- | :--- |
| `>>` | `[Command]`&nbsp;`>>`&nbsp;`[/File]` <details> <summary>Eg.</summary> `echo`&nbsp;`"some text"`&nbsp;`>>`&nbsp;`myFile.txt` </details> | Append Output Redirection | Append the output of the Command to the File. Creates a new File if the specified File does not jet exist. |
| `>` | `[Command]`&nbsp;`>`&nbsp;`[/File]` | Override, Output Redirection | Override the File with the output of the Command. Creates a new File if the specified File does not jet exist. |

| Operation | Usage | Name | Description 
| :---: | :---------- | :--- | :--- |
| `>>` | `[Command]`&nbsp;`>>`&nbsp;`[/File]` `echo`&nbsp;`"some text"`&nbsp;`>>`&nbsp;`myFile.txt` `cat`&nbsp;`FileB`&nbsp;`>>`&nbsp;`FileA.txt` | Append Output Redirection | Append the output of the Command to the File. Creates a new File if the specified File does not jet exist. |
| `>` | `[Command]`&nbsp;`>`&nbsp;`[/File]` | Override, Output Redirection | Override the File with the output of the Command. Creates a new File if the specified File does not jet exist. |

| Type | Usage | Description |
| :---: | :--- | :--- |
| **%** | `echo`&nbsp;`"Some text"`&nbsp;`>>`&nbsp;`myFile.txt` | Append "Some text" to the end of myFile.txt. |
| **%** | `cat`&nbsp;`myFileA.txt`&nbsp;`>>`&nbsp;`myFileB.txt` | Append the contents of a FileA to the end of FileB. |



<kbd>Command</kbd> + <kbd>C</kbd>






