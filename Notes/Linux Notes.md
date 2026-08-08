
# Linux Notes

## 1. Command Line Basics

### GUI vs CLI

- **GUI (Graphical User Interface):** Interact with the system using windows, icons, and buttons.
- **CLI (Command Line Interface):** Interact with the system by typing commands.

### Terminal vs Shell vs Bash

- **Terminal:** The interface/program used to access the command line.
- **Shell:** Interprets commands and communicates with the operating system.
- **Bash:** A popular type of Shell used in Linux.

Common Shells:
- Bash
- Zsh
- Fish

### Command Structure

```bash
command [options] [arguments]
````

Example:

```bash
ls -la Documents
```

* `ls` → Command
* `-la` → Options
* `Documents` → Argument

---

## 2. Basic Commands

### `echo`

Prints text to the terminal.

```bash
echo Hello World
```

### `pwd`

**Print Working Directory**

Shows the current directory.

```bash
pwd
```

### `ls`

Lists the contents of the current directory.

```bash
ls
```

Useful options:

```bash
ls -l    # Detailed information
ls -a    # Show hidden files
ls -la   # Detailed + hidden files
```

### `cd`

**Change Directory**

Used to navigate between directories.

```bash
cd Documents
cd ..
cd
```

* `cd Documents` → Move into `Documents`
* `cd ..` → Move to the parent directory
* `cd` → Return to Home Directory

---

## 3. Navigation & Paths

### Path

A **Path** specifies the location of a file or directory.

Example:

```text
/home/user/Documents/file.txt
```

### Absolute Path

A complete path starting from the Root Directory `/`.

```text
/home/user/Documents
```

### Relative Path

A path based on the current directory.

```bash
cd Documents
```

### Important Path Symbols

| Symbol | Meaning           |
| ------ | ----------------- |
| `/`    | Root Directory    |
| `~`    | Home Directory    |
| `.`    | Current Directory |
| `..`   | Parent Directory  |

---

## 4. Files & Directories

### Root Directory

The top level of the Linux file system:

```text
/
```

> Root Directory `/` is different from the `root` user.

### Home Directory

The user's personal directory.

```text
~
```

### Hidden Files

Files starting with `.` are hidden by default.

Examples:

```text
.bashrc
.config
```

Show them using:

```bash
ls -a
```

### Case Sensitivity

Linux is **case-sensitive**.

```text
file.txt
File.txt
```

These are treated as different names.

### File Extensions

Linux does not rely on file extensions alone to determine file types.

Use:

```bash
file filename
```

to identify a file's type.

---

## 5. Terminal Shortcuts

### Command History

```text
↑  Previous command
↓  Newer command
```

### Tab Completion

Press `Tab` to automatically complete a command, file, or directory name.

If multiple matches exist, pressing `Tab` again can show the available options.

---

## 6. Bash Variables

`$` is used to access the value of a variable.

Example:

```bash
echo $SHELL
```

* `SHELL` → Variable name
* `$SHELL` → Variable value

---

## 7. Manual Pages

### `man`

Used to access the manual/documentation of a command.

```bash
man ls
```

Common sections:

* **NAME** → Command name and purpose.
* **SYNOPSIS** → Command syntax.
* **DESCRIPTION** → Command explanation.
* **OPTIONS** → Available options.

Press:

```text
q
```

to exit the manual page.

---

# Quick Reference

| Command  | Purpose                      |
| -------- | ---------------------------- |
| `echo`   | Print text                   |
| `pwd`    | Show current directory       |
| `ls`     | List directory contents      |
| `ls -l`  | Show detailed information    |
| `ls -a`  | Show hidden files            |
| `ls -la` | Show detailed + hidden files |
| `cd`     | Change directory             |
| `cd ..`  | Move to parent directory     |
| `file`   | Identify file type           |
| `man`    | Open command manual          |

---

# Key Concepts

* **CLI** — Command Line Interface
* **Terminal** — Interface for using the command line
* **Shell** — Interprets and executes commands
* **Bash** — A type of Shell
* **Command** — The instruction being executed
* **Option / Flag** — Modifies a command's behavior
* **Argument** — Information passed to a command
* **Path** — Location of a file or directory
* **Absolute Path** — Full path from `/`
* **Relative Path** — Path based on the current directory
* **Root Directory** — `/`
* **Home Directory** — `~`
* **Current Directory** — `.`
* **Parent Directory** — `..`

```
```
