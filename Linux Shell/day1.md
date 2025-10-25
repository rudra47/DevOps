**১. VirtualBox Setup:**

```
Download থেকে শুরু:
1. VirtualBox download (virtualbox.org) - Windows version
2. Ubuntu 22.04 LTS ISO download (ubuntu.com)
3. VirtualBox install করুন
4. Settings check করুন
```

**২. Ubuntu VM তৈরি:**

```
VM Configuration:
- Name: DevOps-Practice
- Type: Linux
- Version: Ubuntu (64-bit)
- Memory: 4096 MB (4GB)
- Hard Disk: 50 GB (dynamically allocated)
- Network: NAT (default)
```

**৩. Ubuntu Installation:**

- ISO select করে start করুন
- Installation steps follow করুন
- Username: devops (simple রাখুন)
- Password: strong password set করুন
- Installation সময়: 20-30 minutes

**Terminal এ First Commands:**

```bash
# Open the Terminal (Ctrl+Alt+T)

# 1. Where am I?
pwd

# 2. What's here?
ls
ls -l    # detailed view
ls -la   # including hidden files

# 3. Navigate
cd Documents
pwd
cd ..    # go back
cd ~     # home directory

# 4. Create folders
mkdir projects
mkdir projects/laravel
mkdir -p projects/docker/app    # create nested folders

# 5. Create files
touch test.txt
echo "Hello DevOps" > hello.txt
cat hello.txt    # read file
```

**Practice Task:**

```bash
# Practice:
projects/
├── laravel/
│   ├── app1/
│   └── app2/
├── docker/
└── notes/
    └── day1.txt (write your learnings here)