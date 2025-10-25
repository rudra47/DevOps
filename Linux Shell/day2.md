### Day 2: File Operations + Text Editing

**Morning (2 hours):**

**১. File Operations:**

```bash
# Copy files
cp source.txt destination.txt
cp file.txt ~/Documents/    # copy to Documents
cp -r folder1/ folder2/     # copy folder (recursive)

# Move/Rename
mv oldname.txt newname.txt
mv file.txt ~/Documents/

# Delete (careful!)
rm file.txt
rm -r folder/    # delete folder
rm -rf folder/   # force delete (dangerous!)

# View files
cat file.txt           # full content
head file.txt          # first 10 lines
tail file.txt          # last 10 lines
tail -f logfile.log    # follow live logs (important!)
less file.txt          # scrollable view (q to quit)
```

**২. Text Editing - Nano (easier) এবং Vim (powerful):**

**Nano (শুরুতে এটা use করুন):**

```bash
nano myfile.txt

# Inside nano:
# - Type normally
# - Ctrl+O : Save
# - Ctrl+X : Exit
# - Ctrl+K : Cut line
# - Ctrl+U : Paste
```

**Vim basics (gradually শিখবেন):**

```bash
vim myfile.txt

# Vim modes:
# 1. Normal mode (default) - navigation
# 2. Insert mode - typing (press 'i')
# 3. Command mode - save/quit (press ':')

# Essential commands:
# i        : insert mode (start typing)
# Esc      : back to normal mode
# :w       : save
# :q       : quit
# :wq      : save and quit
# :q!      : quit without saving
# /search  : search text
# dd       : delete line
# yy       : copy line
# p        : paste
```

**Practice Task:**

```bash
# 1. Create a file with 20 lines
nano practice.txt
# Write 20 lines about what you learned

# 2. Operations
head -5 practice.txt    # first 5 lines
tail -5 practice.txt    # last 5 lines

# 3. Create backup
cp practice.txt practice.backup.txt

# 4. Edit using vim
vim practice.txt
# Add "Edited in Vim" at top
```

**Evening (1-2 hours):**

**৩. Searching + Finding:**

```bash
# Find text in files
grep "error" logfile.txt
grep -r "TODO" projects/    # search in all files
grep -i "error" file.txt     # case insensitive
grep -i -r "error" file.txt # search in all files with case insensitive

# Find files
find . -name "*.txt"
find . -type f -name "test*"
find /home -size +100M       # files larger than 100MB

# Which command location
which php
which python3
```

**Mini Project:**
```bash
# Laravel error log analyzer script
# Create: analyze_logs.sh

#!/bin/bash
echo "=== Laravel Error Log Analyzer ==="
echo "Searching for errors..."

grep -i "error" storage/logs/laravel.log | head -20
echo ""
echo "Total errors found:"
grep -i "error" storage/logs/laravel.log | wc -l
```
