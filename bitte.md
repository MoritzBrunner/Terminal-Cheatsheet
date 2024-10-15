# Mac Terminal Cheatsheet - Basics with Examples

<table>
  <tr>
    <th align="center">✏️</th>
    <th align="left">File Content</th>
  </tr>
  <tr>
    <td align="center">%</td>
    <td><code>[Command]</code> <code>>></code> <code>[/file]</code></td>
  </tr>
  <tr>
    <td></td>
    <td>
      Append the output of the command to the end of the file. <br>
      <details> 
        <blockquote>
          Official Name: Append Output Redirection
        </blockquote>
        <blockquote>
          <code>echo</code> <code>"some text"</code> <code>>></code> <code>file.txt</code><br>
          Appends <em>some text</em> to the end of file.
        </blockquote>
        <blockquote>
          <code>cat</code> <code>fileA.txt</code> <code>>></code> <code>fileB.txt</code><br>
          Appends the contents of fileA to the end of fileB.
        </blockquote>
        <blockquote>
          <code>pbpaste</code> <code>>></code> <code>file.txt</code><br>
          Appends the content of the systems clipboard to the end of file.
        </blockquote>
        <blockquote>
          <code>grep</code> <code>"searchTerm"</code> <code>fileA.txt</code> <code>>></code> <code>fileB.txt</code><br>
          Appends all lines of fileA that contain <em>searchTerm</em> to the end of fileB.
        </blockquote>
        <blockquote>
          Tip: Creates a new file if the specified file does not exist jet.
        </blockquote>
      </details>
    </td>
  </tr>
  <tr>
    <td align="center">%</td>
    <td><code>[Command]</code> <code>></code> <code>[/file]</code></td>
  </tr>
  <tr>
    <td></td>
    <td>
      Override the contents of the file with the output of the command. <br> 
      <details> 
        <blockquote>
          Official Name: Output Redirection
        </blockquote>
        <blockquote>
          <code>echo</code> <code>"some text"</code> <code>></code> <code>file.txt</code><br>
          Overrides the contents of file with <em>some text</em>.
        </blockquote>
        <blockquote>
          <code>cat</code> <code>fileA.txt</code> <code>></code> <code>fileB.txt</code><br>
          Overrides the contents of fileB with the contents of fileA.
        </blockquote>
        <blockquote>
          <code>pbpaste</code> <code>></code> <code>file.txt</code><br>
          Overrides the content of file with the content of the systems clipboard.
        </blockquote>
        <blockquote>
          <code>history</code> <code>></code> <code>file.txt</code><br>
          Updates the outdated command history of the terminal stored in file with the uptodate command history.
        </blockquote>
        <blockquote>
          Tip: Creates a new file if the specified file does not exist jet.
        </blockquote>
        <blockquote>
          Tip: This operation delets the contents of the target file if it already exists!
        </blockquote>
      </details>
    </td>
  </tr>
  <tr>
    <td align="center">%</td>
    <td><code>[Command]</code> <code>&lt;&lt;EOF</code></td>
  </tr>
  <tr>
    <td></td>
    <td>
      Allows multi-line input to a command until a line with the maker <code>EOF</code> is entered. <br> 
      <details> 
        <blockquote>
          Official Name: Here Document
        </blockquote>
        <blockquote>
          <code>cat</code> <code>&lt;&lt;EOF</code> <code>&gt;&gt;</code> <code>file.txt</code><br>
          Appends all subsequent lines to the end of file till a line with <code>EOF</code> is detected.
        </blockquote>
        <blockquote>
          Tip: In order to end the input <code>EOF</code> must be entered in a fresh line with one space behind it.
        </blockquote>
        <blockquote>
          Tip: <code>EOF</code> is short for end of file.
        </blockquote>
        <blockquote>
          Tip: You can also set another delimiter than <code>EOF</code> to mark the end of the input but <code>EOF</code> is what is most commonly used. 
        </blockquote>
      </details>
    </td>
  </tr>
  <tr>
    <td align="center">%</td>
    <td><code>[Command]</code> <code>&lt</code></td>
  </tr>
  <tr>
    <td></td>
    <td>
      Use the content of a file as input for a command. <br> 
      <details> 
        <blockquote>
          Official Name: Input Redirection
        </blockquote>
        <blockquote>
          <code>pbcopy</code> <code>&lt;</code> <code>file.txt</code><br>
          Sends the content of file to the system clipboard. The same can be archived with:<br>
          <code>cat</code> <code>file.txt</code> <code>|</code> <code>pbcopy</code>
        </blockquote>
        <blockquote>
          Tip: Niche but usefull if you want to shorten some imputs.
        </blockquote>
      </details>
    </td>
  </tr>
  <tr>
    <td align="center">%</td>
    <td><code>pbcopy</code></td>
  </tr>
  <tr>
    <td></td>
    <td>
      Copies the output of a command to the system clipboard. <br> 
      <details> 
        <blockquote>
          Official Name: Copy to Clipboard
        </blockquote>
        <blockquote>
          <code>echo</code> <code>"some text"</code> <code>|</code> <code>pbcopy</code><br>
          Copies <em>some text</em> to the system clipboard.
        </blockquote>
        <blockquote>
          <code>pbcopy</code> <code>&lt;</code> <code>file.txt</code><br>
          Copies the content of file to the system clipboard. The same can be archived with: <br>
          <code>cat</code> <code>file.txt</code> <code>|</code> <code>pbcopy</code>
        </blockquote>
        <blockquote>
          <code>history</code> <code>|</code> <code>pbcopy</code><br>
          Copies the terminals command history to the system clipboard.
        </blockquote>
        <blockquote>
          Tip: You can paste the copied content anywhere by pressing <kbd>Command</kbd> + <kbd>V</kbd>.
        </blockquote>
      </details>
    </td>
  </tr>
  <tr>
    <td align="center">%</td>
    <td><code>pbpaste</code></td>
  </tr>
  <tr>
    <td></td>
    <td>
      Pastes the content of the system clipboard into a file or a command. <br> 
      <details> 
        <blockquote>
          <code>pbpaste</code> <code>&gt;&gt;</code> <code>file.txt</code><br>
          Write the content of the clipboard to file.
        </blockquote>
        <blockquote>
          <code>pbpaste</code> <code>|</code> <code>wc</code><br>
          Count the words of the clipbords content.
        </blockquote>
        <blockquote>
          <code>pbpaste</code> <code>|</code> <code>grep</code> <code>"searchTerm"</code><br>
          Find lines that contain <em>searchTerm</em> in the clipbords content.
        </blockquote>
        <blockquote>
          Tip: This allows you to use content from the system clipboard that was copied with <kbd>Command</kbd> + <kbd>C</kbd> or cut with <kbd>Command</kbd> + <kbd>X</kbd>.
        </blockquote>
      </details>
    </td>
  </tr>
</table>









<table>
  <tr>
    <th align="center">✏️</th>
    <th align="left">Action</th>
    <th align="left">Description</th>
  </tr>
  <tr>
    <td align="center">%</td>
    <td>
      <code>[Command]</code> <code>>></code> <code>[/file]</code>
    </td>
    <td>
      Append the output of the command to the end of the file. 
      <details> 
        <blockquote>
          Official Name: Append Output Redirection
        </blockquote>
        <blockquote>
          <code>echo</code> <code>"some text"</code> <code>>></code> <code>file.txt</code><br>
          Appends <em>some text</em> to the end of file.
        </blockquote>
        <blockquote>
          <code>cat</code> <code>fileA.txt</code> <code>>></code> <code>fileB.txt</code><br>
          Appends the contents of fileA to the end of fileB.
        </blockquote>
        <blockquote>
          <code>pbpaste</code> <code>>></code> <code>file.txt</code><br>
          Appends the content of the systems clipboard to the end of file.
        </blockquote>
        <blockquote>
          <code>grep</code> <code>"searchTerm"</code> <code>fileA.txt</code> <code>>></code> <code>fileB.txt</code><br>
          Appends all lines of fileA that contain <em>searchTerm</em> to the end of fileB.
        </blockquote>
        <blockquote>
          Tip: Creates a new file if the specified file does not exist jet.
        </blockquote>
      </details>
    </td>
  </tr>
  <tr>
    <td align="center">%</td>
    <td>
      <code>[Command]</code> <code>></code> <code>[/file]</code>
    </td>
    <td>
      Override the contents of the file with the output of the command.
      <details> 
        <blockquote>
          Official Name: Output Redirection
        </blockquote>
        <blockquote>
          <code>echo</code> <code>"some text"</code> <code>></code> <code>file.txt</code><br>
          Overrides the contents of file with <em>some text</em>.
        </blockquote>
        <blockquote>
          <code>cat</code> <code>fileA.txt</code> <code>></code> <code>fileB.txt</code><br>
          Overrides the contents of fileB with the contents of fileA.
        </blockquote>
        <blockquote>
          <code>pbpaste</code> <code>></code> <code>file.txt</code><br>
          Overrides the content of file with the content of the systems clipboard.
        </blockquote>
        <blockquote>
          <code>history</code> <code>></code> <code>file.txt</code><br>
          Updates the outdated command history of the terminal stored in file with the uptodate command history.
        </blockquote>
        <blockquote>
          Tip: Creates a new file if the specified file does not exist jet.
        </blockquote>
        <blockquote>
          Tip: This operation delets the contents of the target file if it already exists!
        </blockquote>
      </details>
    </td>
  </tr>
  <tr>
    <td align="center">%</td>
    <td><code>[Command]</code> <code>&lt;&lt;EOF</code></td> 
    <td>
      Allows multi-line input to a command until a line with the maker <code>EOF</code> is entered.
      <details> 
        <blockquote>
          Official Name: Here Document
        </blockquote>
        <blockquote>
          <code>cat</code> <code>&lt;&lt;EOF</code> <code>&gt;&gt;</code> <code>file.txt</code><br>
          Appends all subsequent lines to the end of file till a line with <code>EOF</code> is detected.
        </blockquote>
        <blockquote>
          Tip: In order to end the input <code>EOF</code> must be entered in a fresh line with one space behind it.
        </blockquote>
        <blockquote>
          Tip: <code>EOF</code> is short for end of file.
        </blockquote>
        <blockquote>
          Tip: You can also set another delimiter than <code>EOF</code> to mark the end of the input but <code>EOF</code> is what is most commonly used. 
        </blockquote>
      </details>
    </td>
  </tr>
  <tr>
    <td align="center">%</td>
    <td>
      <code>[Command]</code> <code>&lt</code>
    </td>
    <td>
      Use the content of a file as input for a command.
      <details> 
        <blockquote>
          Official Name: Input Redirection
        </blockquote>
        <blockquote>
          <code>pbcopy</code> <code>&lt;</code> <code>file.txt</code><br>
          Sends the content of file to the system clipboard. The same can be archived with:<br>
          <code>cat</code> <code>file.txt</code> <code>|</code> <code>pbcopy</code>
        </blockquote>
        <blockquote>
          Tip: Niche but usefull if you want to shorten some imputs.
        </blockquote>
      </details>
    </td>
  </tr>
  <tr>
    <td align="center">%</td>
    <td>
      <code>pbcopy</code>
    </td>
    <td>
      Copies the output of a command to the system clipboard.
      <details> 
        <blockquote>
          Official Name: Copy to Clipboard
        </blockquote>
        <blockquote>
          <code>echo</code> <code>"some text"</code> <code>|</code> <code>pbcopy</code><br>
          Copies <em>some text</em> to the system clipboard.
        </blockquote>
        <blockquote>
          <code>pbcopy</code> <code>&lt;</code> <code>file.txt</code><br>
          Copies the content of file to the system clipboard. The same can be archived with: <br>
          <code>cat</code> <code>file.txt</code> <code>|</code> <code>pbcopy</code>
        </blockquote>
        <blockquote>
          <code>history</code> <code>|</code> <code>pbcopy</code><br>
          Copies the terminals command history to the system clipboard.
        </blockquote>
        <blockquote>
          Tip: You can paste the copied content anywhere by pressing <kbd>Command</kbd> + <kbd>V</kbd>.
        </blockquote>
      </details>
    </td>
  </tr>
  <tr>
    <td align="center">%</td>
    <td>
      <code>pbpaste</code>
    </td>
    <td>
      Pastes the content of the system clipboard into a file or a command.
      <details> 
        <blockquote>
          Official Name: Paste to Clipboard
        </blockquote>
        <blockquote>
          <code>pbpaste</code> <code>&gt;&gt;</code> <code>file.txt</code><br>
          Paste the content of the system clipboard to the end of file.
        </blockquote>
        <blockquote>
          <code>pbpaste</code> <code>|</code> <code>wc</code><br>
          Count the words of the system clipbords content.
        </blockquote>
        <blockquote>
          <code>pbpaste</code> <code>|</code> <code>grep</code> <code>"searchTerm"</code><br>
          Find lines that contain <em>searchTerm</em> in the system clipbords content.
        </blockquote>
        <blockquote>
          Tip: This allows you to use content from the system clipboard that was copied with <kbd>Command</kbd> + <kbd>C</kbd> or cut with <kbd>Command</kbd> + <kbd>X</kbd>.
        </blockquote>
      </details>
    </td>
  </tr>
</table>















<table>
  <tr>
    <th align="center">✏️</th>
    <th align="left">Action</th>
    <th align="left">Description</th>
  </tr>
  
  <tr>
    <td align="center">%</td>
    <td><code>cd</code> <code>[directory]</code></td>
    <td>
      Change the current directory to the specified directory.
      <details> 
        <blockquote>
          Official Name: Change Directory
        </blockquote>
        <blockquote>
          <code>cd</code> <code>/path/to/directory</code><br>
          Navigates to <em>/path/to/directory</em>.
        </blockquote>
        <blockquote>
          <code>cd</code> <code>..</code><br>
          Moves one directory up.
        </blockquote>
        <blockquote>
          <code>cd</code> <code>-</code><br>
          Returns to the previous directory.
        </blockquote>
        <blockquote>
          Tip: If no directory is specified, <code>cd</code> takes you to your home directory.
        </blockquote>
      </details>
    </td>
  </tr>

  <tr>
    <td align="center">%</td>
    <td><code>ls</code> <code>[options]</code></td>
    <td>
      List directory contents.
      <details> 
        <blockquote>
          Official Name: List Directory Contents
        </blockquote>
        <blockquote>
          <code>ls</code><br>
          Lists files and folders in the current directory.
        </blockquote>
        <blockquote>
          <code>ls -l</code><br>
          Lists files with detailed information (permissions, size, owner, etc.).
        </blockquote>
        <blockquote>
          <code>ls -a</code><br>
          Lists all files, including hidden ones.
        </blockquote>
        <blockquote>
          Tip: Combine options, e.g., <code>ls -la</code> for a long listing with hidden files.
        </blockquote>
      </details>
    </td>
  </tr>
  
  <tr>
    <td align="center">%</td>
    <td><code>mkdir</code> <code>[directory]</code></td>
    <td>
      Create a new directory.
      <details> 
        <blockquote>
          Official Name: Make Directory
        </blockquote>
        <blockquote>
          <code>mkdir</code> <code>myFolder</code><br>
          Creates a folder named <em>myFolder</em>.
        </blockquote>
        <blockquote>
          <code>mkdir -p</code> <code>/path/to/directory</code><br>
          Creates nested directories if they don’t exist.
        </blockquote>
        <blockquote>
          Tip: The <code>-p</code> option prevents errors if the directory already exists.
        </blockquote>
      </details>
    </td>
  </tr>
  
  <tr>
    <td align="center">%</td>
    <td><code>touch</code> <code>[file]</code></td>
    <td>
      Create a new empty file or update the timestamp of an existing file.
      <details> 
        <blockquote>
          Official Name: Touch File
        </blockquote>
        <blockquote>
          <code>touch</code> <code>newFile.txt</code><br>
          Creates a new file called <em>newFile.txt</em>.
        </blockquote>
        <blockquote>
          Tip: If the file already exists, <code>touch</code> updates its last modification time.
        </blockquote>
      </details>
    </td>
  </tr>

  <tr>
    <td align="center">%</td>
    <td><code>rm</code> <code>[file]</code></td>
    <td>
      Remove (delete) a file or directory.
      <details> 
        <blockquote>
          Official Name: Remove File or Directory
        </blockquote>
        <blockquote>
          <code>rm</code> <code>file.txt</code><br>
          Deletes <em>file.txt</em>.
        </blockquote>
        <blockquote>
          <code>rm -r</code> <code>folder/</code><br>
          Recursively deletes a directory and its contents.
        </blockquote>
        <blockquote>
          Tip: Be cautious! There is no undo for the <code>rm</code> command.
        </blockquote>
      </details>
    </td>
  </tr>
  
  <tr>
    <td align="center">%</td>
    <td><code>cp</code> <code>[source] [destination]</code></td>
    <td>
      Copy files or directories.
      <details> 
        <blockquote>
          Official Name: Copy File or Directory
        </blockquote>
        <blockquote>
          <code>cp</code> <code>fileA.txt</code> <code>fileB.txt</code><br>
          Copies <em>fileA.txt</em> to <em>fileB.txt</em>.
        </blockquote>
        <blockquote>
          <code>cp -r</code> <code>folderA/</code> <code>folderB/</code><br>
          Recursively copies the contents of <em>folderA</em> to <em>folderB</em>.
        </blockquote>
        <blockquote>
          Tip: The <code>-r</code> option is essential when copying directories.
        </blockquote>
      </details>
    </td>
  </tr>
  
  <tr>
    <td align="center">%</td>
    <td><code>mv</code> <code>[source] [destination]</code></td>
    <td>
      Move or rename files and directories.
      <details> 
        <blockquote>
          Official Name: Move or Rename
        </blockquote>
        <blockquote>
          <code>mv</code> <code>oldName.txt</code> <code>newName.txt</code><br>
          Renames <em>oldName.txt</em> to <em>newName.txt</em>.
        </blockquote>
        <blockquote>
          <code>mv</code> <code>file.txt</code> <code>/new/directory/</code><br>
          Moves <em>file.txt</em> to a new directory.
        </blockquote>
        <blockquote>
          Tip: Use <code>mv</code> for both moving and renaming files.
        </blockquote>
      </details>
    </td>
  </tr>
  
  <tr>
    <td align="center">%</td>
    <td><code>cat</code> <code>[file]</code></td>
    <td>
      Display the contents of a file.
      <details> 
        <blockquote>
          Official Name: Concatenate and Print Files
        </blockquote>
        <blockquote>
          <code>cat</code> <code>file.txt</code><br>
          Displays the content of <em>file.txt</em> in the terminal.
        </blockquote>
        <blockquote>
          <code>cat</code> <code>fileA.txt</code> <code>fileB.txt</code> <code>&gt; combined.txt</code><br>
          Combines <em>fileA</em> and <em>fileB</em> into <em>combined.txt</em>.
        </blockquote>
        <blockquote>
          Tip: Use <code>cat</code> with <code>|</code> to pipe the output to another command.
        </blockquote>
      </details>
    </td>
  </tr>
  
</table>
