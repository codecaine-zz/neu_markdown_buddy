### Table of Contents

1.  [What is `micro`?](https://www.google.com/search?q=%231-what-is-micro)
2.  [Prerequisites](https://www.google.com/search?q=%232-prerequisites)
3.  [Installation](https://www.google.com/search?q=%233-installation)
4.  [Basic Usage & The Interface](https://www.google.com/search?q=%234-basic-usage--the-interface)
5.  [Essential Keybindings](https://www.google.com/search?q=%235-essential-keybindings)
6.  [The Command Bar (`Ctrl+E`)](https://www.google.com/search?q=%236-the-command-bar-ctrle)
7.  [Interactive Example: Editing a File](https://www.google.com/search?q=%237-interactive-example-editing-a-file)
8.  [Uninstallation](https://www.google.com/search?q=%238-uninstallation)

-----

### 1\. What is `micro`?

`micro` is a modern and intuitive terminal-based text editor. It aims to be a successor to the `nano` editor and a more user-friendly alternative to complex editors like `vim` and `emacs`. Its key advantage is the use of familiar, universal keybindings (like `Ctrl+S` for save and `Ctrl+C` for copy), making it easy to pick up for anyone who has used a graphical text editor. It also includes modern features like syntax highlighting, split panes, and a robust plugin system.

### 2\. Prerequisites

You must have [Homebrew](https://brew.sh/) installed. You can verify your installation by running:

```bash
brew --version
```

### 3\. Installation

Install `micro` using a single Homebrew command:

```bash
brew install micro
```

### 4\. Basic Usage & The Interface

You can open an existing file or create a new one by providing its name as an argument.

  * **Command:**

    ```bash
    # Create or open a shell script
    micro my_script.sh
    ```

  * **The Main Interface:**
    When you run the command, `micro` opens a clean, modern editor interface within your terminal.

    **Example Interface:**

    ```text
    1 │ #!/usr/bin/env bun
    2 │ 
    3 │ // A simple Bun script
    4 │ console.log("Hello from Bun!");
    5 │ 
    ~
    ~
    ~
    "~/projects/my_script.sh" 5L, 64B [typescript]
    Help: ctrl-g, Save: ctrl-s, Find: ctrl-f, Quit: ctrl-q, Command: ctrl-e
    ```

    The interface consists of the main editing area with line numbers and a status bar at the bottom showing the file path, line/byte count, detected file type, and a hint bar with common commands.

### 5\. Essential Keybindings

`micro` uses keyboard shortcuts that are common in most desktop applications.

  * **File Operations:**

      * `Ctrl+S`: **Save** the current file.
      * `Ctrl+Q`: **Quit**. If there are unsaved changes, it will prompt you to save first.
      * `Ctrl+O`: **Open** a file (will show a file prompt).
      * `Ctrl+G`: Show the main **help** file.

  * **Editing & Selection:**

      * `Ctrl+C`: **Copy** the selected text.
      * `Ctrl+X`: **Cut** the selected text.
      * `Ctrl+V`: **Paste** the text from the clipboard.
      * `Ctrl+Z`: **Undo** the last action.
      * `Ctrl+Y`: **Redo** the last undone action.
      * `Ctrl+D`: **Duplicate** the current line or selection.
      * `Shift` + Arrow Keys: Select text.

  * **Searching:**

      * `Ctrl+F`: **Find**. Opens a search prompt at the bottom.
      * `Ctrl+N`: Find the **next** occurrence.
      * `Ctrl+P`: Find the **previous** occurrence.
      * `Ctrl+A`: **Select all** text in the buffer.

### 6\. The Command Bar (`Ctrl+E`)

Pressing `Ctrl+E` opens a command bar at the bottom, similar to the command palette in VS Code or Sublime Text. Here you can type commands for more advanced actions.

  * **Common Commands:**

      * `vsplit <filename>`: Opens `<filename>` in a **vertical split**.
      * `hsplit <filename>`: Opens `<filename>` in a **horizontal split**.
      * `replace`: Opens a prompt to find and replace text.
      * `goto <line_number>`: Jumps to a specific line number.
      * `save <new_filename>`: Saves the current buffer to a new file.

    **Example Command Bar View:** After pressing `Ctrl+E` and typing.

    ```text
    "~/projects/my_script.sh" 5L, 64B [typescript]
    > vsplit another_script.sh_
    ```

### 7\. Interactive Example: Editing a File

Let's find a setting in a configuration file, change it, and save.

1.  **Open the file:**
    ```bash
    micro ~/.gitconfig
    ```
2.  **Find the relevant section:**
      * Press `Ctrl+F`. The search prompt appears at the bottom.
      * Type `[user]` and press `Enter`. The cursor will jump to the first match.
3.  **Edit the text:**
      * Use the arrow keys to move the cursor to the line with your email address.
      * Edit the line directly, just as you would in any other editor.
4.  **Save the file:**
      * Press `Ctrl+S`. The status bar will flash a "Saved..." message.
5.  **Quit the editor:**
      * Press `Ctrl+Q` to close `micro` and return to your shell prompt.

### 8\. Uninstallation

If you need to remove `micro`, you can do so easily with Homebrew.

```bash
brew uninstall micro
```