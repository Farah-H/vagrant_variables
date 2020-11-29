# Bash Cheat Sheet 
This repository will focus on terminal commands and explaining some advanced topics.

## Files

- No extensions files are just files that can have different formats
- Case sensitive
- Spaces are hard - should be avoided

``bash
mkdir my documents
mkdir "my documents"

cd my\ documents/
``

- `rm`
- `rm -rf` for directiories
- Hidden files and folders are defined with `.` at the beginning
- Display all files with `ls -a` or `ll -a` even hidden
- Flags for bash commands are options
- Check options using `man <command>`

## Permission 
User, group and other

Use binary
- Execute is 1 
- write is 2 
- read is 4

You can combine these to make a maximum of 7 options.

You can also use add and remocing of persions using alias of r (read), w(write) and e(execute)

You can also alias the user (u), group (g) and other (o).

## Root user is a superuser:
You can escalate privilidges using `sudo` command. 

You can also make user `sudo users` list in the system to make other users super users. 

# Head, Tail and Sort 
```bash
head -n 2 example.txt
tail -n 2 example.txt
```

## Streams 

### Standard In - STDIN
### Standard OUT - STOUT
### Standard Error - STDERR


# Going back to the jsnode thing 
```bash
echo "EXPORT DB_HOST='<ipaddress>`" >> ~/.bashrc
```