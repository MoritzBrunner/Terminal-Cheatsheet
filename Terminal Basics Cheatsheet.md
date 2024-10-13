# Terminal Basics Cheatsheet with Examples
# Terminal Cheatsheet - Basics

## File Manipulation
<table>
  <thead>
    <tr>
      <th>Operation</th>
      <th>Usage</th>
      <th>Name</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr> 
      <td align="center" valign="top">
        <code>&gt;&gt;</code>
      </td>
      <td valign="top">
        <code>[Command]</code>&nbsp;<code>&gt;&gt;</code>&nbsp;<code>[/File]</code>
        <details>
          <summary>Eg.</summary>
          <blockquote>
            <code>echo</code>&nbsp;<code>"some text"</code>&nbsp;<code>&gt;&gt;</code>&nbsp;<code>yourFile.txt</code><br>
            Appends <em>some text</em> to the end of yourFile.
          </blockquote>
          <blockquote>
            <code>cat</code>&nbsp;<code>yourFileB.txt</code>&nbsp;<code>&gt;&gt;</code>&nbsp;<code>yourFileA.txt</code><br>
            Appends the contents of yourFileB to the end of yourFileA.
          </blockquote>
          <blockquote>
            <code>history</code>&nbsp;<code>&gt;&gt;</code>&nbsp;<code>yourFile.txt</code><br>
            Appends the this terminals command history to the end of yourFile.
          </blockquote>
          <blockquote>
            <code>pbpaste</code>&nbsp;<code>&gt;&gt;</code>&nbsp;<code>yourFile.txt</code><br>
            Appends the content of the systems clipboard to the end of yourFile.
          </blockquote>
        </details>
      </td>
      <td valign="top"> 
        Append, Output Redirection
      </td>
      <td valign="top"> 
        Append the output of a command to a file.
        <details>
          <summary>Tips:</summary>
          <blockquote>
            Tip: Creates a new file if the specified file does not exist yet.
          </blockquote>
        </details>
      </td>
    </tr>
    <tr> 
      <td align="center" valign="top">
        <code>&gt;</code>
      </td>
      <td valign="top">
        <code>[Command]</code>&nbsp;<code>&gt;</code>&nbsp;<code>[/File]</code>
        <details>
          <summary>Eg.</summary>
          <blockquote>
            <code>echo</code>&nbsp;<code>"some text"</code>&nbsp;<code>&gt;</code>&nbsp;<code>yourFile.txt</code><br>
            Overrides the contents of yourFile with <em>some text</em>.
          </blockquote>
          <blockquote>
            <code>cat</code>&nbsp;<code>yourFileB.txt</code>&nbsp;<code>&gt;</code>&nbsp;<code>yourFileA.txt</code><br>
            Overrides the contents of yourFileA with the contents of yourFileB.
          </blockquote>
          <blockquote>
            <code>history</code>&nbsp;<code>&gt;</code>&nbsp;<code>yourHistoryFile.txt</code><br>
            Updates yourHistoryFile by overriding its contents with the up to date history of this terminal.
          </blockquote>
          <blockquote>
            <code>pbpaste</code>&nbsp;<code>&gt;</code>&nbsp;<code>yourFile.txt</code><br>
            Overrides the content of yourFile with the content of the system clipboard.
          </blockquote>
        </details>
      </td>
      <td valign="top"> 
        Override, Output Redirection
      </td>
      <td valign="top"> 
        Override the content of a file with the output of a command.
        <details>
          <summary>Tips:</summary>
          <blockquote>
            Tip: This operation deletes the existing content of the specified file!
          </blockquote>
          <blockquote>
            Tip: Creates a new file if the specified file does not exist yet.
          </blockquote>
        </details>
      </td>
    </tr>
    <tr> 
      <td align="center" valign="top">
        <code>&lt;&lt;EOF</code>
      </td>
      <td valign="top">
        <code>[Command]</code> <code>&lt;&lt;EOF</code><br>
        <details>
          <summary>Eg.</summary>
          <blockquote>
            <code>cat</code> <code>&lt;&lt;EOF</code> <code>&gt;&gt;</code> <code>yourFile.txt</code><br>
            Appends all subsequent lines to the end of yourFile till a line with <code>EOF </code> is detected.
          </blockquote>
        </details>
      </td>
      <td valign="top"> 
        Multi-Line Input, Here Document
      </td>
      <td valign="top"> 
        Allows multi-line input to a command until a line with the maker <code>EOF </code> is entered.
        <details>
          <summary>Tips:</summary>
          <blockquote>
            Tip: In order to end the input <code>EOF</code> must be typed in a fresh line and with one space behind it.
          </blockquote>
          <blockquote>
            Tip: <code>EOF</code> is short for end of file.
          </blockquote>
          <blockquote>
            Tip: You can set any custom delimiter to mark the end of the input not only <code>EOF</code>. 
          </blockquote>
        </details>
      </td>
    </tr>
    <tr>
      <td align="center" valign="top">
        <code>&lt;</code>
      </td>
      <td valign="top">
        <code>[Command]</code> <code>&lt;</code> <code>[/File]</code>
        <details>
          <summary>Eg.</summary>
          <blockquote>
            <code>pbcopy</code> <code>&lt;</code> <code>yourFile.txt</code><br>
            Sends the content of yourFile to the system clipboard, which is a shorter version of the equivalent:<br>
            <code>cat</code> <code>yourFile.txt</code> <code>|</code> <code>pbcopy</code>
          </blockquote>
        </details>
      </td>
      <td valign="top"> 
        Extract, Input Redirection
      </td>
      <td valign="top"> 
        Use the content of a file as input for a command.
        <details>
          <summary>Tips:</summary>
          <blockquote>
            Tip: Niche but usefull if you want to shorten some imputs.
          </blockquote>
        </details>
      </td>
    </tr>
    <tr> 
      <td align="center" valign="top">
        <code>pbcopy</code>
      </td>
      <td valign="top">
        <details>
          <summary>Eg.</summary>
          <blockquote>
            <code>echo</code> <code>"some text"</code> <code>|</code> <code>pbcopy</code><br>
            Copies <em>some text</em> to the system clipboard.
          </blockquote>
          <blockquote>
            <code>cat</code> <code>yourFile.txt</code> <code>|</code> <code>pbcopy</code><br>
            Sends the content of yourFile to the system clipboard, which is a longer version of the equivalent:<br>
            <code>pbcopy</code> <code>&lt;</code> <code>yourFile.txt</code><br>
          </blockquote>
          <blockquote>
            <code>history</code> <code>|</code> <code>pbcopy</code><br>
            Sends the terminals command history to the system clipboard.
          </blockquote>
        </details>
      </td>
      <td valign="top"> 
        Paste Board Copy, Copy to Clipboard
      </td>
      <td valign="top"> 
        Sends the output of a command to the system clipboard.
        <details>
          <summary>Tips:</summary>
          <blockquote>
            Tip: You can paste the copied content anywhere by pressing <kbd>Command</kbd> + <kbd>V</kbd>.
          </blockquote>
        </details>
      </td>
    </tr>
    <tr> 
      <td align="center" valign="top">
        <code>pbpaste</code>
      </td>
      <td valign="top">
        <details>
          <summary>Show</summary>
          <blockquote>
            <code>pbpaste &gt; yourFile.txt</code><br>
            Writes the content of the clipboard to yourFile.
          </blockquote>
        </details>
      </td>
      <td valign="top"> 
        Paste Board Paste, Paste from Clipboard
      </td>
      <td valign="top"> 
        Sends the content of the system clipboard into a file or a command.
        <details>
          <summary>Tips:</summary>
          <blockquote>
            Tip: This allows you to use content from the system clipboard that was copied with <kbd>Command</kbd> + <kbd>C</kbd> or cut with <kbd>Command</kbd> + <kbd>X</kbd>.
          </blockquote>
        </details>
      </td>
    </tr>
  </tbody>
</table>






<table>
  <thead>
    <tr>
      <th>Operation</th>
      <th>Examples</th>
      <th>Name</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr> 
      <td align="center" valign="top">
        <code>&gt;&gt;</code>
      </td>
      <td valign="top">
        <details>
          <summary>Show</summary>
          <blockquote>
            <code>echo</code>&nbsp;<code>"some text"</code>&nbsp;<code>&gt;&gt;</code>&nbsp;<code>yourFile.txt</code><br>
            Appends <em>some text</em> to the end of yourFile.
          </blockquote>
          <blockquote>
            <code>cat</code>&nbsp;<code>yourFileB.txt</code>&nbsp;<code>&gt;&gt;</code>&nbsp;<code>yourFileA.txt</code><br>
            Appends the contents of yourFileB to the end of yourFileA.
          </blockquote>
          <blockquote>
            <code>history</code>&nbsp;<code>&gt;&gt;</code>&nbsp;<code>yourFile.txt</code><br>
            Appends the this terminals command history to the end of yourFile.
          </blockquote>
          <blockquote>
            <code>pbpaste</code>&nbsp;<code>&gt;&gt;</code>&nbsp;<code>yourFile.txt</code><br>
            Appends the content of the systems clipboard to the end of yourFile.
          </blockquote>
        </details>
      </td>
      <td valign="top"> 
        Append, Output Redirection
      </td>
      <td valign="top"> 
        Append the output of a command to a file.
        <details>
          <summary>Tips:</summary>
          <blockquote>
            Tip: Creates a new file if the specified file does not exist yet.
          </blockquote>
        </details>
      </td>
    </tr>
    <tr> 
      <td align="center" valign="top">
        <code>&gt;</code>
      </td>
      <td valign="top">
        <details>
          <summary>Show</summary>
          <blockquote>
            <code>echo</code>&nbsp;<code>"some text"</code>&nbsp;<code>&gt;</code>&nbsp;<code>yourFile.txt</code><br>
            Overrides the contents of yourFile with <em>some text</em>.
          </blockquote>
          <blockquote>
            <code>cat</code>&nbsp;<code>yourFileB.txt</code>&nbsp;<code>&gt;</code>&nbsp;<code>yourFileA.txt</code><br>
            Overrides the contents of yourFileA with the contents of yourFileB.
          </blockquote>
          <blockquote>
            <code>history</code>&nbsp;<code>&gt;</code>&nbsp;<code>yourHistoryFile.txt</code><br>
            Updates yourHistoryFile by overriding its contents with the up to date history of this terminal.
          </blockquote>
          <blockquote>
            <code>pbpaste</code>&nbsp;<code>&gt;</code>&nbsp;<code>yourFile.txt</code><br>
            Overrides the content of yourFile with the content of the system clipboard.
          </blockquote>
        </details>
      </td>
      <td valign="top"> 
        Override, Output Redirection
      </td>
      <td valign="top"> 
        Override the content of a file with the output of a command.
        <details>
          <summary>Tips:</summary>
          <blockquote>
            Tip: This operation deletes the existing content of the specified file!
          </blockquote>
          <blockquote>
            Tip: Creates a new file if the specified file does not exist yet.
          </blockquote>
        </details>
      </td>
    </tr>
    <tr> 
      <td align="center" valign="top">
        <code>&lt;&lt;EOF</code>
      </td>
      <td valign="top">
        <details>
          <summary>Show</summary>
          <blockquote>
            <code>cat</code> <code>&lt;&lt;EOF</code> <code>&gt;&gt;</code> <code>yourFile.txt</code><br>
            Appends all subsequent lines to the end of yourFile till a line with <code>EOF </code> is detected.
          </blockquote>
        </details>
      </td>
      <td valign="top"> 
        Multi-Line Input, Here Document
      </td>
      <td valign="top"> 
        Allows multi-line input to a command until a line with the maker <code>EOF </code> is entered.
        <details>
          <summary>Tips:</summary>
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
      <td align="center" valign="top">
        <code>&lt;</code>
      </td>
      <td valign="top">
        <details>
          <summary>Show</summary>
          <blockquote>
            <code>pbcopy</code> <code>&lt;</code> <code>yourFile.txt</code><br>
            Sends the content of yourFile to the system clipboard. The same can be archived with:<br>
            <code>cat</code> <code>yourFile.txt</code> <code>|</code> <code>pbcopy</code>
          </blockquote>
        </details>
      </td>
      <td valign="top"> 
        Extract, Input Redirection
      </td>
      <td valign="top"> 
        Use the content of a file as input for a command.
        <details>
          <summary>Tips:</summary>
          <blockquote>
            Tip: Niche but usefull if you want to shorten some imputs.
          </blockquote>
        </details>
      </td>
    </tr>
    <tr> 
      <td align="center" valign="top">
        <code>pbcopy</code>
      </td>
      <td valign="top">
        <details>
          <summary>Show</summary>
          <blockquote>
            <code>echo</code> <code>"some text"</code> <code>|</code> <code>pbcopy</code><br>
            Copies <em>some text</em> to the system clipboard.
          </blockquote>
          <blockquote>
            <code>pbcopy</code> <code>&lt;</code> <code>yourFile.txt</code><br>
            Copies the content of yourFile to the system clipboard. The same can be archived with:<br>
            <code>cat</code> <code>yourFile.txt</code> <code>|</code> <code>pbcopy</code>
          </blockquote>
          <blockquote>
            <code>history</code> <code>|</code> <code>pbcopy</code><br>
            Copies the terminals command history to the system clipboard.
          </blockquote>
        </details>
      </td>
      <td valign="top"> 
        Paste Board Copy, Copy to Clipboard
      </td>
      <td valign="top"> 
        Sends the output of a command to the system clipboard.
        <details>
          <summary>Tips:</summary>
          <blockquote>
            Tip: You can paste the copied content anywhere by pressing <kbd>Command</kbd> + <kbd>V</kbd>.
          </blockquote>
        </details>
      </td>
    </tr>
    <tr> 
      <td align="center" valign="top">
        <code>pbpaste</code>
      </td>
      <td valign="top">
        <details>
          <summary>Show</summary>
          <blockquote>
            <code>pbpaste &gt; yourFile.txt</code><br>
            Writes the content of the clipboard to yourFile.
          </blockquote>
        </details>
      </td>
      <td valign="top"> 
        Paste Board Paste, Paste from Clipboard
      </td>
      <td valign="top"> 
        Sends the content of the system clipboard into a file or a command.
        <details>
          <summary>Tips:</summary>
          <blockquote>
            Tip: This allows you to use content from the system clipboard that was copied with <kbd>Command</kbd> + <kbd>C</kbd> or cut with <kbd>Command</kbd> + <kbd>X</kbd>.
          </blockquote>
        </details>
      </td>
    </tr>
  </tbody>
</table>
