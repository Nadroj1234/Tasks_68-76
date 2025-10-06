# Tasks 68-76

## Lesson 1:

pwd - tells you the current directory your in

mkdir -v (name of directory) - creates a new directory

mkdir -vp dir2/dir3/dir4 - creates multiple directories at once

### listing repositories
ls - list the repositories

ls -R - list all of the repositories made

### moving in repositories
cd dir2 - moves into the repository

cd .. - moves to the parent directory

cd -   - moves to the previous directory

cd - moves to the home directory

_________________________________________________________________________________

## Lesson 2:

### creating file
touch file1.txt - creates a new .txt file names file1

dir - lists the repositories

clear - clears the screen

### displaying message
echo "hello"  - displays "hello" on the screen

echo "hello" >> hello.txt - appends "hello" to the hello.txt file

### displaying contents of file
cat hello.txt - view all contents of hello.txt

head -2 hello.txt - displays the first 2 elements in hello.txt

tail -2 hello.txt - display the last elements in hello.txt

tail hello.txt - displays the last 10 lines in hello.txt

stat hello.txt - displays the details of the file hello.txt

stat dir1 - displays the details abou the directory dir1

_________________________________________________________________________________

## Lesson 3:

du - displays the disk usage of current directory

du -xh ~  - use h switch to output in a human readable format and the x switch to exclude other file systems and ~ denotes your home

du --max-depth 3 ~  - du can take a long time so you can specify the max.directory depth 

### copying files
cp -v hello.txt dir2 - copies the hello.txt file to directory dir2

cp -v hello.txt dir2/file2.txt - This will copy hello.txt into dir2 at the same time, rename it as "file2.txt".

cp  -vr dir2/*.txt dir2/dir3 - This will copy all files ending with ".txt" from dir2 into dir2/dir3.

cp -vr dir2/dir3  .  - copies the directory named "dir3" to current directory

### displaying file or directory data
md5sum hello.txt - if the file is too large use this instead of "cat"

md5sum dir2/hello.txt - displays the same info as the one above

md5sum hello.txt - displays the same info as the one above

### renaming files
mv hello.txt dir2/dir3/dir4/hi.txt - will move file "hello.txt" into directory "dir4" and renames it "hi.txt"
When you use cp there exists two copies of a file (similar to copy-paste "ctrl-c" and "ctrl-v") with mv there is one copy (its cut-paste ctrl-x and ctrl-v). unlike (cp,rm) other commands mv don't need "-r" for directories.

mkdir dir5 - to create a new directory


mv dir2/*.txt dir5 - moves all ".txt" files under dir2 into dir5
mv dir5  dir50 - renames "dir5" as "dir50"

ln  dir2/dir3/dir4/hi.txt hello - creates a link and you can now edit "dir2/dir3/dir4/hi.txt" as "hello"

ln -s  dir2/dir3/dir4/hi.txt  softlink - creates a softlink 

### deleting files
rm -i file2.txt - removes individual file

rm -rf junk/* 
rmdir  dir50 - removes empty directory

_________________________________________________________________________________

## Lesson 4:

### basic process commands

