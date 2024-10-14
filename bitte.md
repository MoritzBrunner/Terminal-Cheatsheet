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
