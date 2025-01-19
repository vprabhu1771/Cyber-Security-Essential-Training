# 9 - Text Editors
 
1. **nano**

Nano is a popular text editor for the command line in Unix-like operating systems. Here are some common shortcuts and commands you can use in Nano:

**Opening and Saving Files:**
- nano filename: Open a file for editing.
- Ctrl + O: Save changes to the current file (you'll be prompted to confirm the filename).
- Ctrl + X: Exit Nano (you'll be prompted to save changes if any have been made).

**Basic Editing:**
- Arrow keys: Navigate through the text.
- Ctrl + K: Cut (delete) the current line.
- Ctrl + U: Uncut (paste) the previously cut text.
- Ctrl + _ (underscore): Go to a specific line and column.
- Alt + U: Undo the last action.
- Alt + E: Redo the last undone action.

**Selecting Text:**
- Ctrl + Shift + 6: Start selecting text.
- Use arrow keys to select text.
- Ctrl + K: Cut (delete) the selected text.
- Ctrl + U: Uncut (paste) the selected text.

**Search and Replace:**
- Ctrl + W: Search for text within the file.
- Ctrl + \: Search and replace text.
- Alt + W: Repeat the last search.

**Navigation and Bookmarks:**
- Alt + \: Set a bookmark at the current cursor position.
- Ctrl + ]: Go to the next bookmark.
- Ctrl + [: Go to the previous bookmark.

**Working with Multiple Files:**
- Ctrl + R: Insert the contents of another file into the current buffer.

**Miscellaneous:**
- Ctrl + G: Display the help menu, showing various commands.
- Ctrl + C: Show current cursor position (line and column).
- Ctrl + T: Enable/disable line wrapping.

These are some of the most commonly used shortcuts in Nano, but there are many more available. You can always access the Nano help menu by pressing Ctrl + G to see a list of available commands and shortcuts.

Remember that Nano is designed to be user-friendly and straightforward, making it an excellent choice for beginners to text editing in the command line.


2. **vim**

Vim is a highly configurable text editor known for its efficiency and power. It has a steep learning curve, but mastering its shortcuts can greatly boost your productivity. Here's a list of some essential Vim shortcuts and commands:

**Modes:**
1. **Normal Mode (Command Mode)**: This is the default mode for navigation and issuing commands.
2. **Insert Mode**: In this mode, you can insert and edit text.
3. **Visual Mode**: Used for text selection.

**Basic Navigation:**
- h: Move left (in normal mode).
- j: Move down (in normal mode).
- k: Move up (in normal mode).
- l: Move right (in normal mode).
- w: Move to the beginning of the next word.
- b: Move to the beginning of the previous word.
- e: Move to the end of the current word.
- 0: Move to the beginning of the line.
- $: Move to the end of the line.
- G: Move to the end of the file.
- gg: Move to the beginning of the file.
- <line_number>G: Move to a specific line number.

**Editing:**
- i: Enter insert mode before the cursor.
- I: Enter insert mode at the beginning of the line.
- a: Enter insert mode after the cursor.
- A: Enter insert mode at the end of the line.
- o: Open a new line below the current line.
- O: Open a new line above the current line.
- x: Delete the character under the cursor.
- dd: Delete the current line.
- yy: Yank (copy) the current line.
- p: Paste after the cursor.
- P: Paste before the cursor.
- u: Undo the last action.
- Ctrl + r: Redo the last undone action.

**Visual Mode (Text Selection):**
- v: Start visual mode to select text character by character.
- V: Start visual mode to select whole lines.
- Ctrl + v: Start visual block mode to select a rectangular block of text.

**Searching and Replacing:**
- /search_term: Search for a term (use n to find the next occurrence).
- ?search_term: Search backward.
- :s/old/new/g: Replace 'old' with 'new' in the entire line.
- :%s/old/new/g: Replace 'old' with 'new' in the entire file.

**Saving and Exiting:**
- :w: Save changes.
- :q: Quit Vim (if no changes are made).
- :q!: Quit Vim without saving changes.
- :wq or :x: Save and quit.

**Other Useful Commands:**
- :e filename: Open a new file.
- :bn or :bp: Move to the next or previous buffer.
- :sp or :vsp: Split the window horizontally or vertically.
- :set number: Display line numbers.
- :set nonumber: Hide line numbers.

These are just some of the many Vim commands and shortcuts. Vim has a rich set of features and customization options, so you can tailor it to your specific needs. To learn more and become proficient with Vim, consider using the built-in help system (:help) or referring to external resources and tutorials.

3. **emacs**

Emacs is a highly customizable text editor with a vast number of keyboard shortcuts and commands. Below is a list of some commonly used Emacs shortcuts. Keep in mind that Emacs can be extended with various packages, so there may be additional shortcuts specific to those packages.

**Basic Editing:**

1. **File Operations**
   - C-x C-f: Open a file.
   - C-x C-s: Save the current file.
   - C-x C-w: Save as (write to a different file).
   - C-x C-c: Quit Emacs.

2. **Cut, Copy, and Paste**
   - C-space: Set the mark (start of the selection).
   - C-w: Cut (kill) the selected text.
   - M-w: Copy (kill-ring) the selected text.
   - C-y: Paste (yank) the text from the kill-ring.

3. **Undo and Redo**
   - C-/ or C-x u: Undo.
   - M-/: Redo.

4. **Cursor Movement**
   - C-f: Move forward one character.
   - C-b: Move backward one character.
   - C-n: Move to the next line.
   - C-p: Move to the previous line.
   - M-<: Move to the beginning of the buffer.
   - M->: Move to the end of the buffer.

**Text Manipulation:**

5. **Search and Replace**
   - C-s: Search forward.
   - C-r: Search backward.
   - M-% or C-M-%: Query replace.

6. **Indentation and Formatting**
   - M-x indent-region: Indent the selected region.
   - M-x untabify: Convert tabs to spaces.
   - M-x tabify: Convert spaces to tabs.

**Buffers and Windows:**

7. **Buffer Management**
   - C-x b: Switch to another buffer.
   - C-x k: Kill (close) the current buffer.
   - C-x left/right arrow: Switch to the previous/next buffer.

8. **Window Management**
   - C-x 2: Split the window vertically.
   - C-x 3: Split the window horizontally.
   - C-x 0: Delete the current window.
   - C-x 1: Delete all other windows and keep the current one.
   - C-x o: Switch between windows.
   - C-x 5 2: Open a new frame (window).

**Advanced Editing:**

9. **Macros**
   - C-x (: Start recording a macro.
   - C-x ): Stop recording a macro.
   - C-x e: Execute the last recorded macro.

10. **Marking and Region**
    - C-SPC: Set the mark.
    - C-x h: Select the entire buffer (mark whole buffer).
    - M-x narrow-to-region: Restrict editing to the current region.

11. **Commenting**
    - M-;: Comment or uncomment the current line or region.

12. **Completion**
    - M-/ or M-x dabbrev-expand: Expand text using completion.

These are just a subset of the many keyboard shortcuts available in Emacs. Emacs is highly extensible, so you can define your own shortcuts and customize it to suit your needs. You can also install various packages to add additional functionality and shortcuts.