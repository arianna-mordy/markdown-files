# MATLAB Resource

## 1. What is MATLAB?

MATLAB is both a programming language and an interactive environment well utilized by researchers for versatile reasons like running programs and analyzing data. While MATLAB has a graphical interface with point and click on icons to run commands ("MATLAB Desktop"), MATLAB primarily operates through a command line interface. 

### Applications in Research:

- Advanced statistical testing and data fitting
- Automate routine data processing tasks
- Designing and executing complex experimental tasks, including real-time data collection and behavioral tracking
- Develop computational models and apply machine learning algorithms
- Processing and analyzing neuroimaging data

This resource will focus on the basics of MATLAB to develop the skills necessary for using MATLAB in neuroimaging data analysis. 

## 2. Workspace Basics

### MATLAB Desktop Interface:

When you first open MATLAB, you will notice that it has several windows and a ribbon of buttons at the top. The window on the left is the **Current Folder**, the central window is the **Command Window**, and the upper-right window is the **Workspace**.

- **Current Folder:** Shows a list of all the folders located within the folder you are currently in. (This is essentially your window.)
  
- **Command Window:** The main area where you can type commands directly and see their output.
  
- **Editor Window:** Where you writing, running, and debugging MATLAB code
  
- **Workspace Window:** Displays variables created during the session, providing an overview of the data you are working with.

![image](https://github.com/user-attachments/assets/27b88c90-33be-4848-a7ee-04495f7446e0)


### Custimization and Setting Preferences

MATLAB offers flexible customization options to optimize your workflow. Some ways to tailor the interface include...

- **Resize and Reposition Windows:** Adjust the size and position of MATLAB windows by clicking and dragging the window dividers or title bars to suit your preferences.
- **Save Frequently Used Commands :** The Favorites menu allows you to bookmark commonly used commands. Add a command by selecting 'New Favorite,' entering the command, and giving it a descriptive name. For quicker access, add these favorites to the Quick Access toolbar and execute them with a single click.
- **Display Variable Details:** To gain more insights into the variables you're working with, such as their types or memory usage, right-click the header bar in the Workspace window and choose the properties you wish to display.

For more advanced customizations, navigate to **Preferences** under the Home tab.
<img width="1000" alt="image" src="https://github.com/user-attachments/assets/cdc7c230-c22d-41e6-917a-ec8468bc5eeb">


### Directories:

MATLAB organizes folders and files using a directory tree, starting with the root directory (/). 

- **Absolute Path:** Specifies the entire path from the root directory. E.g., `ls /Users/your-username`
  
- **Relative Path:** Specifies the path relative to the current directory. E.g., `cd Desktop`


### Commands for Navigating Workspace

| Command          | Description                                           |
|------------------|-------------------------------------------------------|
| `pwd`            | Prints the current working directory path. |
| `cd 'folder'`    | Changes the current working directory to 'folder'. |
| `cd ~`           | Changes the current directory to the user's home directory. |
| `cd .`           | Refers to the current directory. |
| `cd ..`          | Moves up one level in the directory tree. |
| `ls`             | Lists all files and directories in the current directory. |
| `dir`            | Lists directory contents, similar to `ls`. |
| `exist 'name'`   | Checks if a variable, file, or folder 'name' exists. |
| `mkdir 'dirname'`| Creates a new directory named 'dirname'. |
| `rmdir 'dirname'`| Removes the directory named 'dirname', if it is empty. |
| `edit 'filename'`   | Opens the specified file in MATLAB's editor.           |
| `edit functionName` | Opens the function in MATLAB's editor   |
| `doc command`    | Opens the documentation for 'command'. |
| `help command`   | Displays help text for 'command' in the Command Window. |
| `clc`            | Clears all input and output from the Command Window, keeping history. |
| `quit` or  `exit`| Closes MATLAB. |



### Keyboard Shortcuts for MATLAB Command Window

This cheat sheet includes common keyboard shortcuts that are handy when coding in MATLAB's Command Window, mirroring the functionality often used in terminal environments.

#### For Windows Users

| Shortcut          | Description                                      |
|-------------------|--------------------------------------------------|
| `Tab`             | Auto-completes commands and variable names based on partially typed text. |
| `Esc`             | Cancels the current command line input without executing it. |
| `Up Arrow`        | Scrolls through the history to recall previous commands, useful for repetition or modification. |
| `Down Arrow`      | Scrolls forward in the command history after using the Up Arrow. |
| `Ctrl + C`        | Interrupts the execution of the current command or script. |
| `Ctrl + A`        | Moves the cursor to the beginning of the line. |
| `Ctrl + E`        | Moves the cursor to the end of the line. |
| `Ctrl + L`        | Clears the screen, keeping the history intact. |
| `Ctrl + Up Arrow` | Scrolls up through the output to view earlier outputs and messages. |
| `Ctrl + Down Arrow` | Scrolls down through the output to return to more recent outputs. |
| `Home`            | Jumps to the beginning of the current line. |
| `End`             | Jumps to the end of the current line. |
| `Backspace`       | Deletes the character to the left of the cursor. |
| `Delete`          | Deletes the character right at the cursor position. |
| `Enter`           | Executes the command currently typed in the Command Window. |
| `Shift + Enter`   | Continues command entry onto the next line for multi-line commands. |

#### For Mac Users

| Shortcut          | Description                                      |
|-------------------|--------------------------------------------------|
| `Tab`             | Auto-completes commands and variable names based on partially typed text. |
| `Esc`             | Cancels the current command line input without executing it. |
| `Up Arrow`        | Scrolls through the history to recall previous commands. |
| `Down Arrow`      | Scrolls forward in the command history after using the Up Arrow. |
| `Cmd + C`         | Interrupts the execution of the current command or script. |
| `Cmd + A`         | Moves the cursor to the beginning of the line. |
| `Cmd + E`         | Moves the cursor to the end of the line. |
| `Cmd + L`         | Clears the screen, keeping the history intact. |
| `Cmd + Up Arrow`  | Scrolls up through the output to view earlier outputs and messages. |
| `Cmd + Down Arrow`| Scrolls down through the output to return to more recent outputs. |
| `Fn + Left Arrow` | Mimics the Home key, jumping to the beginning of the line. |
| `Fn + Right Arrow`| Mimics the End key, jumping to the end of the line. |
| `Delete`          | Deletes the character to the left of the cursor. (Mac keyboards typically do not have a separate Backspace key.) |
| `Fn + Delete`     | Deletes the character right at the cursor position. |
| `Return`          | Executes the command currently typed in the Command Window. |
| `Shift + Return`  | Continues command entry onto the next line for multi-line commands. |

