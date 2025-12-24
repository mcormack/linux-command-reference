# linux-command-reference

<img src="https://www.linuxfoundation.org/hubfs/Tux-flat-version.svg" alt="Linx Mascot - Tux" width="100"/>

## Reference for Linux Commands

* `uname`: Print basic info about system OS and hardware. [**Options**](#uname)
* `pwd`: Print working directory, where are we located.
* `cd`: Change working directory.
* `ls`: Lists / displays contents of a directory. Shows files and directories within the current directory. [**Options**](#ls)
* `cat`: Concatenate: Read the contents of any file. [**Options**](#cat)
* `grep`: General Regular Expression Print: Search for text patterns in files or output. Filters and displays lines that match a specific string or patttern. [**Options**](#grep)
* `cp`: Copy files from one directory to another `cp [SOURCE] [DESTINATION]` [**Options**](#cp)
* `wc`: Word Count: Count number of lines, words, characters in a file or some input. [**Options**](#wc)
* `find`: 
* `diff`: 
* `curl`: Call URL
* `vim`: 
* `chmod`: 
* `touch`: Create files

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

⬆ [**GO UP**](#reference-for-linux-commands)

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

⬆ [**GO UP**](#reference-for-linux-commands)

### cat

* -n: Displays the output with line numbers.
* -E: Displays a $ character at the end of each line.
* -s: Squeezes multiple adjacent empty lines into one.

You can join multiple files into a new file:

```bash
cat file1.txt file2.txt > merged.txt
```

⬆ [**GO UP**](#reference-for-linux-commands)

### grep

* Searching within a specific file:

```bash
grep dog sample.txt
```

* When searching for phrases use "":

```bash
grep "connection refused" sample.txt
```

* -i makes the search case-insensitive.
* Use regex for more advanced seach patterns. Lines that start with Hello for example:

```bash
grep "^Hello" -i sample.txt
```

* More complex search examples 🗒️ [Search Patterns Examples](https://labex.io/tutorials/linux-linux-grep-command-with-practical-examples-422703#use-grep-to-search-for-patterns-in-text-files)

⬆ [**GO UP**](#reference-for-linux-commands)

### cp

#### Examples

Simple Copy

```bash
cp file1.txt file1_copy.txt
```

Copy to another Directory, passing the direct path:

```bash
cp file1.txt /root/file1_copy.txt
```

Also used to copy directories:

```bash
cp -r dir1 dir2
```

* -r used to copy directories recursively, including internal files.
* -p preserve the original file attributes and timestamps

⬆ [**GO UP**](#reference-for-linux-commands)

### wc

* -l Count Lines
* -w Count Words
* -c Bytes
* -m Characters
* -L find longest Line Length

⬆ [**GO UP**](#reference-for-linux-commands)

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

### Other:

Chain multiple commands using the `|` (pipe) operator. Whatever the first command outputs it will be the input of the following command.

```bash
## Chain Commands
cat file1.txt | grep Database
```

Output functions result into a textfile using `>`:

```bash
## Output result to a file
cat file1.txt | grep Database > filtered.txt
```

Append lines to .txt using `>`.

```bash
## Create sample text files
echo "First line of file_1.txt." > file_1.txt
echo "Second line of file_1.txt." >> file_1.txt
```

⬆ [**GO UP**](#reference-for-linux-commands)
