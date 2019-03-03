# Command Line 101 Outline

## What is the Command Line?

- Command Line Structure
  - Prompt
  - Commands
  - Options
  - Arguments
  - Output
- Shell
  - Bash
- Help
  - `man`
    - `q` to quit

## Getting Around

- `pwd`
- `ls`
  - `ls [options] [location]`
  - `ls -l /folder`
  - `ls -a`
- Absolute and Relative Paths
  - Slash vs No Slash
- Path Shortcuts
  - `~`
    - Home
  - `.`
    - Current Directory
  - `..`
    - Parent Directory
- Moving
  - `cd`
    - No path = go home
    - Tab completion
- `ctrl-c`
- Up arrow/History
### Exercise
1. Start at your `home` directory
1. List the contents of the `/etc` directory
1. Switch to the `/etc/network` directory
3. Switch back to your `home` directory in one command
4. Switch back to `/etc/network` without using `cd`

## Files

- Case Sensitive
- Spaces in File Names
  - Quotes
    - Single or Double
  - Escape character
    - `\`
  - Tab completion is your friend
- Hidden Files
  - `ls -a`
- File Directories
  - `mkdir [options] <Directory>`
  - `mkdir -p`
    - Makes parent directories as needed
  - `mkdir -v`
    - Verbose output
  - `rmdir`
    - Directories must be empty
- Files
  - `touch`
    - Creates a blank file
  - `cp [options] <source path> <destination path>`
    - Copy a file or directory
    - `cp -r`
      - Recursive for directories
  - `mv [options] <source> <destination>`
    - Move a file or directory
    - Also renames a file or directory
  - `rm [options] <file>`
    - Remove a file or empty folder
    - NO UNDO!!!!
    - `rm -r`
      - Remove non-empty folders recursively
- Editing Files
  - `nano`
    - `ctrl o`
    - `ctrl x`
  - `vi`
### Exercise
1. Go to your `home` directory
2. Create a file called `brainstorm.txt`
3. Create a folder called `dells`
4. Move the file `brainstorm.txt` into the folder `dells`
5. Make a copy of the `brainstorm.txt` file. Name it whatever you want.
6. Delete the file `brainstorm.txt`
7. Open the file you created in a text editor, and add some text. Save the file.
8. Delete the `dells` folder
## Wildcards

- `*`
  - Zero or more characters
  - `ls *.txt`
- `?`
  - Single character
  - `ls ?o*`
  - `ls *.???`
- `[]`
  - Range of Characters
  - `ls [sv]*` (Name begins with 's' or 'v')

### Exercise
1. Go to your home directory
2. Create three files with the .txt extension, and one file with a .sh extension
3. List all of the .txt files in one command
4. List all of the .sh files in one command

## Permissions

- Verbs
  - `r`
    - read
  - `w`
    - write
  - `x`
    - execute
- Nouns
  - `u`
    - Owner (Single user)
  - `g`
    - Group
  - `o`
    - Other (everyone else)
- Viewing Permissions
  - `ls -l`
    - First character identifies file type
    - Next three = owner
    - Next three = group
    - Next three = other
- Changing Permissions
  - `chmod [permissions][path]`
    - Permissions argument
      - 1 Whose permissions are changing?
      - 2 Are we adding or removing permissions?
      - 3 What permissions are being set?
    - Octal permissions

---

| Octal | Binary |
| ----- | ------ |
| `0`   | `000`  |
| `1`   | `001`  |
| `2`   | `010`  |
| `3`   | `011`  |
| `4`   | `100`  |
| `5`   | `101`  |
| `6`   | `110`  |
| `7`   | `111`  |

`rwx`
`111`

---

- Directories work the same
- Root user
### Exercise
1. Long List the files in your home directory
2. What are the verbs for each file?
3. What are the nouns?
4. Create a folder, name it whatever you want
5. Long list the files again. How can you tell a regular file from a directory
6. Change the permissions on your folder so that only the owner of the file has access
7. Do the same for one of your files, but use the Octal method

## Piping and Redirection

- Three data streams
  - STDIN (0)
  - STDOUT (1)
  - STDERR (2)
- Redirecting
  - `>`
    - `ls > output.txt`
    - Creates a new file, or wipes and recreates existing file
  - `>>`
    - Creates a new file, or appends to existing file

### Exercise 
1. List the files in the /etc directory, but output them into a file called `output.txt`
2. List the files in the /var directory, and put them in the `output.txt` file
3. What happened to the contents?
4. List the file int he /etc directory again, but don't wipe the contents of the `output.txt` file

## Networking

- Ping
- Traceroute
- SSH
- SCP
- ifconfig

### Exercise
1. Start up your server and find the server's IP address
2. Ping the server
3. Log into the server using SSH
4. Run top on the server and see what's running, then quit top
5. Install htop
