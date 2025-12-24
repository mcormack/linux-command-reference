# linux-command-reference

<img src="https://www.linuxfoundation.org/hubfs/Tux-flat-version.svg" alt="Linx Mascot - Tux" width="100"/>

## Reference for Linux Commands

* `uname`: Print basic info about system OS and hardware. [**Options**](#uname)
* `pwd`: Print working directory, where are we located.
* `cd`: Change working directory.
* `ls`: Lists / displays contents of a directory. Shows files and directories within the current directory. [**Options**](#ls)
* `cat`: Concatenate: Read the contents of any file. [**Options**](#cat)
* `grep`: 
* `cp`: 
* `wc`: 
* `find`: 
* `diff`: 
* `curl`: 
* `vim`: 
* `chmod`: 

## 🎥 Good References / Sources

1. 📼 [TechWorld with Nana - 13 Linux Commands](https://www.youtube.com/watch?v=CLh2ACdXNbc): Mentioned Commands:
   * uname, pwd, cd, ls, cat, grep, cp, wc, find, diff, curl, vim, chmod
2. 📋 [Linux Commands Cheat Sheet](https://linux-commands.labex.io/)

## 📋 Extended Reference - Commands' Options

### uname

* -a All System Information
* -s Kernel name (default)
* -r Kernel release
* -v Kernel version
* -m Machine hardware architecture / name (ex., x86_64)
* -n Network hostname
* -o Operating system
* -p Processor type

### ls

#### Most Used

* -l Long format: Shows files details: permisions, owner, size and modification date.
* -h Displays file sizes in human-readable formats (e.g., KB, MB) when combined with -l.
* -t Sorts files by modification time, with the newest first.

#### Other

* -a All files, including hidden ones.
* -R Lists contents of directories recursively, including subdirectories.
* -r Reverses the order of the output.
* -1 Lists one file per line instead of displaying them in columns.
* -d Lists directories only.
* -F Appends a character to filenames indicating their type (e.g., / for directories, * for executables).
* -X Sorts files alphabetically by their extension.

### cat

You can also join multiple files into a new file:

```bash
cat file1.txt file2.txt > merged.txt
```

### grep

* 

### cp:

* 

### wc: 
* 

### find: 
* 

### diff: 
* 

### curl: 
* 

### vim: 
* 

### chmod: 
* 
