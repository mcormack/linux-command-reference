# linux-command-reference

<img src="https://www.linuxfoundation.org/hubfs/Tux-flat-version.svg" alt="Linx Mascot - Tux" width="100"/>

## All Commands and Shortcuts:
* 📋 [IT-Tools Bash Cheatsheet](https://sharevb-it-tools.vercel.app/bash-memo)

## Reference for Linux Commands

* 🖋️ `uname`: Print basic info about system OS and hardware. [**Options**](#uname)
* 📍 `pwd`: Print working directory, where are we located.
* 📂 `cd`: Change working directory.
* 📋`ls`: Lists / displays contents of a directory. Shows files and directories within the current directory. [**Options**](#ls)
* 🐈‍⬛ `cat`: Concatenate: Read the contents of any file. [**Options**](#cat)
* 🔍 `grep`: General Regular Expression Print: Search for text patterns in files or output. Filters and displays lines that match a specific string or patttern. [**Options**](#grep)
* 📮 `cp`: Copy files from one directory to another `cp [SOURCE] [DESTINATION]` [**Options**](#cp)
* 💯 `wc`: Word Count: Count number of lines, words, characters in a file or some input. [**Options**](#wc)
* 🔍 `find`: Search for Files and direcories. `find [starting_path] [option] [expression]`. [**Options**](#find)
* 🚦 `diff`: Compare two files and show the difference. `diff file1 file2` [**Options**](#diff)
* 🕸️ `curl`: Client URL. Used to transfer data from or to a server using HTTP or other protocols. Typically used to interact with APIs. [**Options**](#curl)
* 📝 `vim`: Open VIM Editor to change files. [**Options**](#vim)
* ✍️ `chmod`: Change Mode: Modify file permissions. [**Options**](#chmod)
* ✋ `touch`: Create files or update the timestamps. `touch [options] [file_name(s)]` [**Options**](#touch)

## 🎥 Good References / Sources

1. 📼 [TechWorld with Nana - 13 Linux Commands](https://www.youtube.com/watch?v=CLh2ACdXNbc): Mentioned Commands:
   * uname, pwd, cd, ls, cat, grep, cp, wc, find, diff, curl, vim, chmod
2. 📋 [Linux Commands Cheat Sheet](https://linux-commands.labex.io/)
3. ﹥ Other CLI Tools [10 CLI apps Video](https://www.youtube.com/watch?v=EJ6uvqhKR4M)

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

#### Others

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
* -c display the count of matches.
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

### find

* Options: You can search by name, file type, file size or permission.
* -type: f file, d directory.
* -size: Finding by size, using + and - prefixes signifying greater than and less than. 'M' for mebibytes, 'G' for gibibytes, 'k' for kibibytes.
* Examples:
"."= Current Directory.
"/"= Entire File System. Root file system.

```bash
find -name / "*.conf"
# Combine with grep to filter:
find -name / "*.conf" | grep db
find -name / "*.conf*" | grep db
# Larger files:
find . -size +1M
```

More info: [Linux Manual on Find](https://man7.org/linux/man-pages/man1/find.1.html)

⬆ [**GO UP**](#reference-for-linux-commands)

### diff

* -c: Display the differences in a more readable format.
* -w: Ignore white space differences.

⬆ [**GO UP**](#reference-for-linux-commands)

### curl

* -I (or --head): Just return the headers. (Metadata)
* -O Tells curl to save the file with the same name as the remote file.
* -o To specify a different file name.

```bash
curl https://google.com
curl http://localhost:5432

curl -o curl_homepage.html https://google.com
```

⬆ [**GO UP**](#reference-for-linux-commands)

### vim

* Commonly used for editing config files in Linux
* It has 3 modes
  * Insert Mode: type or edit text.
  * Normal Mode: Default, for navigation
  * Command Mode: Execute commands like save, quit, search.

```bash
vim db.config
```

Navigation:

* To enter edit mode, press i.
* To Exit: Press ESC (Back to normal mode) then ":" and:
  * `:q` Quit only if no changes have been made.
  * `:q!` Quit without Saving
  * `:w` Save the file
  * `:wq` or `ZZ`
  * `x` Save and quit only if changes were made.

⬆ [**GO UP**](#reference-for-linux-commands)

### chmod

* File Permissions

  * Initial symbol: `-` File, `d` Directory, `l` Sybolic Link
  * Different types: `-rwxrwxrwx`: Read, Write, Execute, `-` is denied.
  * Position is in this order: User, Group, Other. so `-rw-rw---` means User and Group can only read and write.
  * To change permissons each permission has a numeric value: r=4, w=2, x=1

```bash
## Full Permissions
chmod 777 db.config
## No Permissions
chmod 000 db.config
## Read Permissions only for all groups
chmod 444 db.config
## Owner rwx, Group and Others: rx (Good for Scripts)
chmod 755 db.config
## Owner rw, Group and Others: r (Usually Text files)
chmod 644 db.config
```

⬆ [**GO UP**](#reference-for-linux-commands)

### touch

* -a: Updates the access time of the file.
* -m: Updates the modification time of the file.
* -d or -t: Sets the access and modification times to the specified date and time.
* -c or -f: Creates the file if it doesn't exist, without issuing an error message.

```bash
touch new_file.txt
```

⬆ [**GO UP**](#reference-for-linux-commands)

### Other

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

## Useful Tools

1. 🛠️ [It Tools](https://it-tools.tech/json-minify) -> [Web Version](https://it-tools.tech/) -> Forked due to non maintenance -> [Next Tools](https://github.com/willjayyyy/next-tools) -> [Web Version](https://www.next-tools.dev/)
