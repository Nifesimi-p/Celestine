**Class Lab: Build a "Company Files" project using terminal commands**

**Step 1: Setup**
```
mkdir -v company_project
cd company_project
pwd
```
Confirms folder created, moves into it, shows path.

**Step 2: Create structure**
```
mkdir -p reports/2025 reports/2026 staff
```
Creates reports folder with two year subfolders, plus a staff folder.
```
ls -R
```
Shows the whole structure they just built.

**Step 3: Create files**
```
touch reports/2025/sales.txt
touch reports/2025/expenses.txt
touch staff/employees.txt
```

**Step 4: Add content**
```
cat > staff/employees.txt
```
Type a few names, press Ctrl+D to save.
```
cat staff/employees.txt
```
Shows what they typed.

**Step 5: Check file type**
```
file staff/employees.txt
```

**Step 6: Copy and rename**
```
cp staff/employees.txt staff/employees_backup.txt
mv staff/employees_backup.txt staff/backup_2025.txt
```

**Step 7: Search inside files**
```
grep -i "john" staff/employees.txt
```
Replace "john" with a name they typed earlier.

**Step 8: Practice head/tail**
```
head -n 3 staff/employees.txt
tail -n 3 staff/employees.txt
```

**Step 9: Sort and count**
```
sort staff/employees.txt
wc -l staff/employees.txt
```

**Step 10: Find files**
```
find . -name "*.txt"
```
Shows every txt file in the project.

**Step 11: Compare files**
```
diff staff/employees.txt staff/backup_2025.txt
```

**Step 12: tee demo**
```
cat staff/employees.txt | tee staff/employees_copy.txt
```
Shows output on screen and saves a copy at the same time.

**Step 13: Cleanup**
```
rm staff/backup_2025.txt
rmdir reports/2026
```
Only works since 2026 folder is empty.

**Step 14: Navigate practice**
```
cd reports/2025
pwd
cd ..
cd -
```

LINUX 3

mkdir practice && cd practice
# create a folder called practice, then move into it

ls -l > filelist.txt
cat filelist.txt
# list files in detail, save the list into filelist.txt (overwrite)
# print filelist.txt content to screen

echo "new line" >> filelist.txt
# add "new line" to the end of filelist.txt, without erasing existing content

wc -l < filelist.txt
# count lines in filelist.txt (file fed in as input)

ls -l | less
# list files, send output into less so you can scroll through it

mkdir docs && touch docs/a.txt docs/b.txt
# create a docs folder, then create two empty files inside it

tar -cvzf docs.tar.gz docs/

tar docs/
# bundle and compress the docs folder into docs.tar.gz
# -c create, -v show files as they're added, -z compress with gzip, -f name the output file

tar -xvzf docs.tar.gz -C /tmp
# extract docs.tar.gz into /tmp
# -x extract, -C set destination folder

chmod 755 filelist.txt
ls -l filelist.txt
# set permissions: owner can read/write/run, group and others can read/run only
# check the permissions were applied

useradd -m student1
# create a new user student1, with a home folder (-m)

passwd student1
# set a password for student1

usermod -aG sudo student1
# add student1 to the sudo group, without removing his other groups
# -a append, -G group

groupadd testers
# create a new group called testers

userdel -rf student1
# delete student1, remove his home folder and mail (-r), force it even if logged in (-f)




FILE|
-r -w -x.        user.    dev.  ot
4.  2  1          OW     G      OT
                  rwx.   rwx.   rwx

                -rw-r--r--
chmod
chown
755
drwxr -xr -x.
-rw- r- -r--.
644