# Terminal Basics Cheatsheet with Examples

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
  </tbody>
</table>
