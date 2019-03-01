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
|-------|--------|
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

## Process Management
- `top`
- `htop`
- `ps ax`

## Scripting

## Networking
- Ping
- Traceroute
- SSH