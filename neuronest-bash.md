### What is Bash?
Bash is a command-line interface (CLI) shell program. The name Bash is an acronym for “Bourne Again SHell,” as it was derived from a shell written by Stephen Bourne. Bash is often the default shell in Unix and in most packages that provide Unix-like tools for Windows. 

### What is a shell?
A “shell”  is a computer program that allows us to control a computer’s operating system (OS) with a command-line interface (CLI) or graphical user interface (GUI). The CLI enables us to send commands to the computer, run processes, and receive outputs. A shell may also be referred to as “command line” or “terminal”.

### What is Unix?
Unix is an operating system. The UNIX operating system is one of the most commonly-used tools for computing, as it is an powerful tool for controlling how the computer executes programs. The Unix shell is both a command-line interface (CLI) and a scripting language that allows users to perform complex tasks like automating repetitive processes, and creating large, efficient workflows.

### How do I install a Shell program?
On Apple's Mac computers, you can find the shell application in your Applications/Utilities folder under the name “Terminal” or click on the Finder magnifying glass, and type "Terminal". On many Linux operating systems, Terminal comes installed with the operating system. On Windows, you can install a shell application by installing [git for Windows](https://gitforwindows.org/). 

If you're having trouble downloading, installing, or accessing your computer's shell application, here are some helpful links:
  
  <https://swcarpentry.github.io/shell-novice/#install-software>
  <https://carpentries.github.io/workshop-template/install_instructions/#shell>

### How do I use the command shell?
Upon opening the shell application, you will see a prompt, which indicates that the shell is ready for input. This prompt is also called the “command line”. The prompt typically ends in a $, but can also end with #, >, %, or %>%. The prompt is followed by a text cursor, a character (usually a flashing or solid block) that indicates the position where your typing will appear. You can type commands into this prompt and press the “enter” or “return” key to execute them. The commands entered at the command line are sent to the computer’s operating system to do a variety of different operations, or to launch various other programs.
Note: Do NOT type the prompt when typing commands. Only type the command that follows the prompt.

## Keyboard Shortcuts for the Command Window

This cheat sheet includes common keyboard shortcuts that are handy when coding in the shell application.

#### For Windows Users

| Shortcut          | Description                                      |
|-------------------|--------------------------------------------------|
| `Tab`             | Auto-completes commands and variable names based on partially typed text. |
| `Up Arrow`        | Scrolls up through the history to recall previous commands, useful for repetition or modification. |
| `Down Arrow`      | Scrolls down in the command history after using the Up Arrow. |
| `Ctrl + C`        | Interrupts the execution of the current command or script. |
| `Ctrl + L`        | Clears the screen, keeping the history intact. |
| `Backspace`       | Deletes the character to the left of the cursor. |
| `Delete`          | Deletes the character right at the cursor position. |
| `Enter`           | Executes the command currently typed in the Command Window. |
| `Shift + Enter`   | Continues command entry onto the next line for multi-line commands. |

#### For Mac Users

| Shortcut          | Description                                      |
|-------------------|--------------------------------------------------|
| `Tab`             | Auto-completes commands and variable names based on partially typed text. |
| `Up Arrow`        | Scrolls through the history to recall previous commands. |
| `Down Arrow`      | Scrolls forward in the command history after using the Up Arrow. |
| `Cmd + C`         | Interrupts the execution of the current command or script. |
| `Cmd + L`         | Clears the last executed command from the screen, keeping the history intact. |
| `Delete`          | Deletes the character to the left of the cursor. |
| `Fn + Delete`     | Deletes the character to the right of the cursor position. |
| `Return`          | Executes the command currently typed in the Command Window. |
| `Shift + Return`  | Continues command entry onto the next line for multi-line commands. |

## Using the shell  

### Directories:

Folders and files are organized using a directory tree, starting with the root directory (/). 
- **Absolute Path:** Specifies the entire path from the root directory. E.g., `ls /Users/your-username`
  
- **Relative Path:** Specifies the path relative to the current directory. E.g., `cd Desktop`

### Commands for Navigating Directories

| Command          | Description                                           |
|------------------|-------------------------------------------------------|
| `pwd`            | Prints the current working directory path. |
| `cd 'folder'`    | Changes the current working directory to 'folder'. |
| `cd ~`           | Changes the current directory to the user's home directory. |
| `cd .`           | Refers to the current directory. |
| `cd ..`          | Moves up one level in the directory tree. |
| `ls`             | Lists all files and directories in the current directory. |
| `mkdir 'dirname'`| Creates a new directory named 'dirname'. |
| `rmdir 'dirname'`| Removes the directory named 'dirname', if it is empty. |
| `nano 'filename'`   | Opens the specified file in nano editor.           |
| `man command`    | Opens the manual for 'command'. |
| `help command`   | Displays help text for 'command' in the Command Window. |
| `exit`           | Exits terminal. |
| `echo $NAME`     | Prints variable. |
| `clear`          | Clears the screen, keeping the history intact. |


## Working With Files and Directories
### Basic Directory Management
Create a New Directory: mkdir [path]
Creates a new directory. Avoid using spaces; underscores are not recommended.
Example: `mkdir results`
The `-p` flag  creates a project directory with two subdirectories (data and results) in the parent directory (one step up).
Example: `mkdir -p ../project/data ../project/results`

###File Creation and Editing
Create or Edit a File: `nano <filename>`
If the file does not exist, it will be created. Type your content, then save and exit.
#### Shortcut Keys in Nano:
  | Command          | Description                                           |
  |------------------|-------------------------------------------------------|
  | `Ctrl + O`       | Save the file (into a current or new name). |
  | `Ctrl + X`       | Exit the editor. If unsaved, nano will prompt to save. |
  | `Ctrl + K`       | Cut (“kill”) a line of text. Repeated use cuts multiple lines. |
  | `Ctrl + U`       | Paste the cut text. |

### File and Directory Operations
Create an Empty File: `touch <filename>`
Creates an empty file. Useful for generating placeholder files required by some programs.

Copy a File: `cp [old] [new]`
Copies a file to a new location. Example: `cp [old].txt ../[new].txt`

Copy a Directory: `cp -r [source] [destination]`
Copies a directory and all its contents.
Move/Rename a File or Directory: `mv [old] [new]`

Remove an Empty Directory: `rmdir [directory]`

Remove a File Permanently: `rm [path]`

Interactive Mode: `rm -i [path]`
Prompts for confirmation before deletion.
Remove a Directory and Its Contents: `rm -r [directory]`

Interactive Mode: `rm -r -i [directory]`
Prompts for confirmation before deletion.
Important Note: Deleted files are gone forever—there is no trash or recycle bin.

Wildcard Characters
* — Matches zero or more characters. Example: *.txt matches all .txt files.
? — Matches any single character. Example: ?.txt matches a.txt but not any.txt.
Pipes and Filters
Pipe Operator: |

Redirects the output of one command into another.
Example: ls | wc
Counts lines, words, and characters in the output of ls.
Redirect Output to a File: command > [file]

Overwrites the file with command output.
Append Output to a File: command >> [file]

Common Commands:

cat: Prints the contents of files. Example: cat file1.txt file2.txt
more: Similar to cat, but displays one page at a time. Spacebar to continue.
less -N [file]: Displays content page by page with line numbers. Use q to exit.
sort [file]: Sorts file contents alphanumerically. Use -n for numerical sorting.
head [file]: Displays the first 10 lines. Use -n [#] to specify the number of lines.
tail [file]: Displays the last 10 lines.
Count and Filter:

wc [file]: Counts lines, words, and characters.
Example: wc -l *.txt outputs the line count for each file.
grep [pattern] [file]: Searches for a pattern in files.
Use -v to exclude lines with the pattern, -i for case-insensitivity.
Example with Pipes:

ls | grep "D" | wc
Counts the number of words containing "D" in the ls output.
Command Redirection
Redirect Output to a File: ls -l > filename.list

Pipe Output to Another Command: cat filename.list | grep keyword > filefound.list

Remove Duplicates: cut -d , -f 2 [file].csv | sort | uniq

cut: Extracts specific columns from a file. Use -d to specify delimiter (default is TAB).


## Understanding Permissions

In Unix-like operating systems, permissions control who can read, modify, or execute files and directories. This is crucial for managing security and access on your system. The way permissions are handled in Unix is somewhat similar to Windows, but the specifics differ.

### Basic Concepts

- **Ownership**: Every file and directory has an owner and a group associated with it. The operating system tracks these using numeric IDs.
- **Categories**: Each user falls into one of three categories for any file:
  - **Owner**: The user who owns the file.
  - **Group**: Users who are part of the file’s associated group.
  - **Others**: Everyone else on the system.

### Permission Types

Permissions specify what actions users in each category can perform:

- **Read (`r`)**: Allows viewing the contents of the file.
- **Write (`w`)**: Allows modifying the file.
- **Execute (`x`)**: Allows running the file if it is a program or script.

### Viewing Permissions

Use the `ls -l` command to view detailed file permissions. The output includes:

- **File Type and Permissions**: A string like `-rwxr-xr-x` that shows permissions:
  - The first character indicates the type (e.g., `-` for files, `d` for directories).
  - The next three characters are the owner's permissions.
  - The following three are the group's permissions.
  - The last three are the permissions for others.

For example, `-rwxr-xr-x` means:
- **Owner**: Can read, write, and execute.
- **Group**: Can read and execute, but not write.
- **Others**: Can read and execute, but not write.

### Changing Permissions

To modify permissions, use the `chmod` command. Here are some common usages:

- **Set Specific Permissions**:
  ```bash
  chmod u=rw final.grd
  ```
 This sets read and write permissions for the owner (u stands for user).
- **Set Permissions for Group**:
  ```bash
  chmod g=r final.grd
    ```
  This grants read-only permissions to the group (g stands for group).
- **Remove All Permissions"
  ```bash
  chmod a= final.grd
  ```
  This removes all permissions for everyone (a stands for all).
  **Using Numerics**
  ```bash
  chmod 770 test.txt
  ```
  This gives read, write, and execute permissions to the owner and group, but no permissions to others.

   - **Make a File Readable**: The chmod command is commonly used to make a file "executable", like this
   ```bash
    chmod +x myShellScript.sh
    ```
  - **Make a Script Executable**: The chmod command is commonly used to make a file "executable", like this
   ```bash
    chmod +x myShellScript.sh
    ```
   
### Special Permissions for Directories




### MATLAB File Types:

- **.m files**: MATLAB script and function files, each serving different purposes:
  - **Script Files**: Scripts are collections of MATLAB commands executed exactly as if they were typed into the Command Window. They operate within the current workspace, which means they can modify any existing variables or create new ones. Scripts do not accept inputs directly (though they can work with data already in the workspace) and do not return outputs. They are useful for straightforward tasks like data manipulation and plotting when you do not need to isolate code.
  - **Function Files**: Functions, on the other hand, are more versatile and encapsulate their code within a separate workspace. They can accept inputs and return outputs, making them essential for modular programming. Functions prevent potential conflicts with the main workspace by keeping variables local, except those explicitly returned. They are ideal for reusing code, enhancing code readability, and managing larger projects where data encapsulation is necessary.

- **.mlx files**: MATLAB live script files that combine code execution with narrative, formatted text, equations, images, and hyperlinks in a single, interactive document. Ideal for instructional purposes, interactive applications, and sharing results.

- **.mat files**: Binary files that store workspace variables. Useful for saving your session data and transferring variables between sessions without losing integrity.

- **.fig files**: Figure files that save MATLAB graphical outputs. They enable you to reopen and modify figures later, preserving the graphical data and properties exactly as saved.


### File Formats for Import and Export

MATLAB supports importing various data formats such as TXT, CSV, XLS, XLSX, JPG, PNG, etc. You can find additional documentation including functions and examples [here](https://www.mathworks.com/help/matlab/import_export/supported-file-formats-for-import-and-export.html).


### Commands for File Handling

| Command                      | Description                                           |
|------------------------------|-------------------------------------------------------|
| `save 'filename'`            | Saves workspace variables to a file.                  |
| `load 'filename'`            | Loads variables from a file into the workspace.       |
| `readtable('filename')`      | Imports data from a file into a table, supporting CSV, TXT, and Excel formats. |
| `readmatrix('filename')`     | Reads numerical data from a file into a matrix, ideal for straightforward data formats. |
| `xlsread('filename')`        | Imports data from Excel files, useful for datasets in spreadsheets. |
| `csvread('filename')`        | Reads numerical data from CSV files directly into an array. |
| `fopen('filename')`          | Opens a file for reading or writing, necessary for file manipulation. |
| `fwrite(fid, data)`          | Writes binary data to the file specified by `fid`.    |
| `fprintf(fid, format, data)` | Writes formatted data to the file, allowing for customizable text outputs. |
| `fclose(fid)`                | Closes an open file to free up resources.             |
| `importdata('filename')`     | Loads mixed data from files, handling various formats automatically. |
| `exportdata('data', 'filename')` | Exports data to a file in chosen formats, useful for sharing or external use. |



### External Tutorial
MATLAB Desktop – Importing Data, Customizing the MATLAB Desktop, and Setting Preferences from MathWorks Self-Paced Online Courses: MATLAB Desktop Tools and Troubleshooting Scripts Course

[Tutorial Link](https://matlabacademy.mathworks.com/details/matlab-desktop-tools-and-troubleshooting-scripts/otmldts)

[Quick Reference](https://matlabacademy.mathworks.com/artifacts/quick-reference.html?course=otmldts&language=en&release=R2024a)


## Basics of MATLAB Syntax

This section provides an overview of fundamental MATLAB syntax, essential for writing and understanding MATLAB code.

#### MATLAB Operators and Special Characters

This section provides an overview of MATLAB operators and special characters, which are essential for writing and understanding MATLAB code.

### Relational Operators

| Operator | Description         | Example       |
|----------|---------------------|---------------|
| `==`     | Equal to            | `a == b`      |
| `~=`     | Not equal to        | `a ~= b`      |
| `>`      | Greater than        | `a > b`       |
| `<`      | Less than           | `a < b`       |
| `>=`     | Greater than or equal to | `a >= b` |
| `<=`     | Less than or equal to    | `a <= b` |

### Logical Operators

| Operator | Description         | Example       |
|----------|---------------------|---------------|
| `&`      | Logical AND         | `a & b`       |
| `|`      | Logical OR          | `a | b`       |
| `~`      | Logical NOT         | `~a`          |
| `xor`    | Logical EXCLUSIVE OR| `xor(a, b)`   |

### Special Characters

| Character | Description         | Example       |
|-----------|---------------------|---------------|
| `:`       | Colon               | `1:10`        |
| `;`       | Semicolon           | `a = 5;`      |
| `%`       | Percent             | `% comment`   |
| `=`       | Assignment Operator | `a = 5`       |
| `.`       | Decimal Point       | `3.14`        |
| `,`       | Comma               | `[1, 2, 3]`   |
| `()`      | Parentheses         | `a(1)`        |
| `[]`      | Square Brackets     | `[1, 2, 3]`   |
| `{}`      | Curly Braces        | `{1, 2, 3}`   |
| `'''`     | Single Quote        | `'text'`      |
| `...`     | Ellipsis            | `a = 1 + ...` (continues on next line) # MATLAB Operators and Special Characters

This section provides an overview of MATLAB operators and special characters, which are essential for writing and understanding MATLAB code.

## Arithmetic Operators

| Operator | Description         | Example       |
|----------|---------------------|---------------|
| `+`      | Addition            | `a + b`       |
| `-`      | Subtraction         | `a - b`       |
| `*`      | Multiplication      | `a * b`       |
| `/`      | Right Division      | `a / b`       |
| `\`      | Left Division       | `a \ b`       |
| `^`      | Power               | `a ^ b`       |
| `.`      | Decimal Point       | `3.14`        |

## Relational Operators

| Operator | Description         | Example       |
|----------|---------------------|---------------|
| `==`     | Equal to            | `a == b`      |
| `~=`     | Not equal to        | `a ~= b`      |
| `>`      | Greater than        | `a > b`       |
| `<`      | Less than           | `a < b`       |
| `>=`     | Greater than or equal to | `a >= b` |
| `<=`     | Less than or equal to    | `a <= b` |

## Logical Operators

| Operator | Description         | Example       |
|----------|---------------------|---------------|
| `&`      | Logical AND         | `a & b`       |
| `|`      | Logical OR          | `a | b`       |
| `~`      | Logical NOT         | `~a`          |
| `xor`    | Logical EXCLUSIVE OR| `xor(a, b)`   |

## Special Characters

| Character | Description         | Example       |
|-----------|---------------------|---------------|
| `:`       | Colon               | `1:10`        |
| `;`       | Semicolon           | `a = 5;`      |
| `%`       | Percent             | `% comment`   |
| `=`       | Assignment Operator | `a = 5`       |
| `.`       | Decimal Point       | `3.14`        |
| `,`       | Comma               | `[1, 2, 3]`   |
| `()`      | Parentheses         | `a(1)`        |
| `[]`      | Square Brackets     | `[1, 2, 3]`   |
| `{}`      | Curly Braces        | `{1, 2, 3}`   |
| `'''`     | Single Quote        | `'text'`      |
| `...`     | Ellipsis            | `a = 1 + ...` (continues on next line) |

### Detailed Usage of Special Characters

- **Colon `:`**
  - Used to create vectors, specify ranges, and index arrays.
  - Example: `1:5` generates a vector `[1, 2, 3, 4, 5]`.
  - Used in array slicing: `A(:, 2)` selects all rows from the second column of matrix `A`.

- **Semicolon `;`**
  - Suppresses the output of a command.
  - Example: `a = 5;` assigns 5 to `a` without displaying the output.
  - Used to separate rows in matrix definitions: `A = [1, 2; 3, 4]`.

- **Percent `%`**
  - Used for comments. Everything after `%` on that line is ignored by MATLAB.
  - Example: `x = 10; % This is a comment`.

- **Assignment Operator `=`**
  - Assigns a value to a variable.
  - Example: `a = 5`.

- **Decimal Point `.`**
  - Indicates decimal numbers.
  - Example: `3.14`.

- **Comma `,`**
  - Separates elements in arrays and function arguments.
  - Example: `[1, 2, 3]` or `plot(x, y)`.

- **Parentheses `()`**
  - Used for grouping expressions, function arguments, and array indexing.
  - Example: `a = (b + c) * d` or `y = myFunction(x)`.

- **Square Brackets `[]`**
  - Used to create arrays and matrices.
  - Example: `A = [1, 2, 3]` or `B = [1, 2; 3, 4]`.

- **Curly Braces `{}`**
  - Used for cell arrays, which can hold different types of data.
  - Example: `C = {1, 'text', [1, 2, 3]}`.

- **Single Quote `'''`**
  - Defines a string.
  - Example: `str = 'Hello, World!'`.

- **Ellipsis `...`**
  - Indicates that a statement continues on the next line.
  - Example:
    ```matlab
    a = 1 + 2 + 3 + ...
        4 + 5 + 6;
    ```

This chart provides a detailed reference for MATLAB operators and special characters, which are fundamental for performing various operations and structuring MATLAB code effectively.


## 4. Working with Variables in MATLAB

This section provides an overview of how to handle variables in MATLAB, including how to create, manipulate, and delete them, as well as working with vectors and matrices.

#### Creating Variables

Variables in MATLAB are created simply by assigning values to them. MATLAB does not require explicit declaration of variable types.

| Command             | Description                                           |
|---------------------|-------------------------------------------------------|
| `x = 5;`            | Creates a variable `x` and assigns it the value `5`.  |
| `name = 'MATLAB';`  | Creates a string variable `name` with the text `MATLAB`. |

#### Working with Vectors

Vectors are a fundamental data structure in MATLAB used to store lists of numbers.

| Command             | Description                                           |
|---------------------|-------------------------------------------------------|
| `v = [1, 2, 3];`    | Creates a row vector `v` with elements 1, 2, and 3.   |
| `w = [1; 2; 3];`    | Creates a column vector `w` with elements 1, 2, and 3.|
| `length(v);`        | Returns the number of elements in vector `v`.         |
| `v(2);`             | Accesses the second element of vector `v`.            |
| `v(1:2);`           | Accesses the first and second elements of vector `v`. |

#### Working with Matrices

Matrices are two-dimensional arrays of numbers. MATLAB is specifically designed to work efficiently with matrices.

| Command             | Description                                           |
|---------------------|-------------------------------------------------------|
| `A = [1, 2; 3, 4];` | Creates a 2x2 matrix `A`.                             |
| `B = zeros(3,3);`   | Creates a 3x3 matrix `B` filled with zeros.           |
| `C = ones(2,4);`    | Creates a 2x4 matrix `C` filled with ones.            |
| `D = eye(3);`       | Creates a 3x3 identity matrix `D`.                    |
| `size(A);`          | Returns the size of matrix `A`.                       |
| `A(2,1);`           | Accesses the element in the second row, first column of `A`. |
| `A(:,2);`           | Accesses all elements in the second column of `A`.    |
| `A(1,:);`           | Accesses all elements in the first row of `A`.        |

#### Manipulating Variables

Once variables are created, they can be manipulated using MATLAB's built-in functions and operators.

| Command             | Description                                           |
|---------------------|-------------------------------------------------------|
| `v = [1, 2, 3];`    | Creates a row vector `v` with elements 1, 2, and 3.   |
| `w = v + 1;`        | Adds `1` to each element of vector `v`.               |
| `u = sum(v);`       | Sums the elements of `v` and stores the result in `u`.|
| `mean(v);`          | Calculates the mean of vector `v`.                    |
| `A = A + 2;`        | Adds `2` to each element of matrix `A`.               |
| `A * 2;`            | Multiplies each element of matrix `A` by `2`.         |
| `A * B;`            | Performs matrix multiplication of `A` and `B`.        |
| `A .* B;`           | Performs element-wise multiplication of `A` and `B`.  |

#### Deleting Variables

To free up resources or clear workspace, you can delete variables that are no longer needed.

| Command             | Description                                           |
|---------------------|-------------------------------------------------------|
| `clear x;`          | Deletes the variable `x` from the workspace.          |
| `clear x y z;`      | Deletes multiple variables `x`, `y`, and `z`.         |
| `clear all;`        | Clears all variables from the workspace.              |

#### Viewing Variables

To view the variables currently stored in your workspace, you can use the Workspace window or specific commands.

| Command             | Description                                           |
|---------------------|-------------------------------------------------------|
| `who;`              | Lists all variables in the workspace.                 |
| `whos;`             | Lists all variables with detailed information including size, bytes, and class. |

These basic commands and techniques provide a foundation for working with varia
