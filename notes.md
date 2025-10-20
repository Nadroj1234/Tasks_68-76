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

cd - - moves to the previous directory

cd - moves to the home directory

---

## Lesson 2:

### creating file

touch file1.txt - creates a new .txt file names file1

dir - lists the repositories

clear - clears the screen

### displaying message

echo "hello" - displays "hello" on the screen

echo "hello" >> hello.txt - appends "hello" to the hello.txt file

### displaying contents of file

cat hello.txt - view all contents of hello.txt

head -2 hello.txt - displays the first 2 elements in hello.txt

tail -2 hello.txt - display the last elements in hello.txt

tail hello.txt - displays the last 10 lines in hello.txt

stat hello.txt - displays the details of the file hello.txt

stat dir1 - displays the details abou the directory dir1

---

## Lesson 3:

du - displays the disk usage of current directory

du -xh ~ - use h switch to output in a human readable format and the x switch to exclude other file systems and ~ denotes your home

du --max-depth 3 ~ - du can take a long time so you can specify the max.directory depth

### copying files

cp -v hello.txt dir2 - copies the hello.txt file to directory dir2

cp -v hello.txt dir2/file2.txt - This will copy hello.txt into dir2 at the same time, rename it as "file2.txt".

cp -vr dir2/\*.txt dir2/dir3 - This will copy all files ending with ".txt" from dir2 into dir2/dir3.

cp -vr dir2/dir3 . - copies the directory named "dir3" to current directory

### displaying file or directory data

md5sum hello.txt - if the file is too large use this instead of "cat"

md5sum dir2/hello.txt - displays the same info as the one above

md5sum hello.txt - displays the same info as the one above

### renaming files

mv hello.txt dir2/dir3/dir4/hi.txt - will move file "hello.txt" into directory "dir4" and renames it "hi.txt"
When you use cp there exists two copies of a file (similar to copy-paste "ctrl-c" and "ctrl-v") with mv there is one copy (its cut-paste ctrl-x and ctrl-v). unlike (cp,rm) other commands mv don't need "-r" for directories.

mkdir dir5 - to create a new directory

mv dir2/\*.txt dir5 - moves all ".txt" files under dir2 into dir5
mv dir5 dir50 - renames "dir5" as "dir50"

ln dir2/dir3/dir4/hi.txt hello - creates a link and you can now edit "dir2/dir3/dir4/hi.txt" as "hello"

ln -s dir2/dir3/dir4/hi.txt softlink - creates a softlink

### deleting files

rm -i file2.txt - removes individual file

rm -rf junk/\*
rmdir dir50 - removes empty directory

---

## Lesson 4:

### basic process commands

### create a process

ps - output is nothing but showing the currently running processes.

sleep 60 & - creates a new process

### kill a process

kill 12345 - this kills the process, replace the 12345 with the sleep process id you got above.

kill -9 12345 - someitmes the process wont die with the simple kill command, use this instead

killall sleep - this will kill all processes witht the name sleep

killall -u webminal - kills only processes owned by user "webminal"

killall -w find - wait for all find processes to die

### return process ID

pidof bash - provides the process ID of a running program bash

pidof -s bash - returns only one process id

### adjust the priority of process

nice -n 19 sleep 30 & - adjust the priority of your process by stating a process like this

renice -n 12345 - adjust the priority of currently with the pid

renice +1 -u webminal - adjust the priority for all process owned by "webminal"

### display all running process

top - displays all running process. (press q to exit the top)

### display tree of process

pstree - displays the process in a tree

pstree -p - display the tree with the ids

time ls -1 - how long it took to complete a command

---

## Lesson 5:

### Maipulate or parse file contents

grep "linux" hello - searches for mathcing words or line on a file

grep -r 'Hello' . - search entire directory files

grep -i 'lINUX' hello - ignore case sensative by using -i

grep -n 'linux' hello - displys line numbers

grep -v 'world' hello - displays lines that dont match the pattern

wc -L hello - counts the lines/words/bytes in a file

cut -f1 -d' ' new.txt - cuts the new file. -f can be used to metion column number and -d is used to specify delimiter

paste hello new.txt - merges the lines of files

paste -s hello new.txt - pastes one file at a time

sort new.txt - sort file content

diff hello linux.txt - compare two files

diff3 hello new.txt linux.txt - compare three files

---

## Lesson 6:

### Changing file attributes

dirname dir2/dir3/dir4/hi.txt - manipulates pathname

basename dir2/dir3/dir4/hi.txt - strips the directory and suffix from pathname and give the last entry

chmod -v 666 file1.txt - changes the file access permission

chmod a+r file1.txt - same as the above command

chmod a-rw file1.txt - makes it so no one can read or write into the file

chmod u+rw file1.txt - only the owner can read or write into the file

chmod -R 644 ~/chmod_dir - change permission for

chown root file1.txt - changing the file owner

chown root:staff file1.txt - change file owner and group

chown root:staff -R ~/dir2 - to change permission on all files and sub-directories, use -R switch

chown --from=webminal:webminal root:staff -R ~/dir2 - will change the files the belong to webminal user and webminal group to root and other user files left as it is

chgrp -hR root dir2 - change the group of dir2 and subfiles to "root"

---

## Lesson 7:

### Locate file and its type

file linux.txt - shows file type

file /dev/null - dertermines the type of file as ASCII text

whereis ls - location of certain file

whereis stdio.h - finding the source file

which php - shows which version will be executed

find ~ -name "linux.txt" - search a file on any directory

find . -type f -exec file '{}' \; - to find regular files and invoke the command on the results

find . -type f -exec ls -l '{}' \; - find regular files and display their strributes using the ls command

find ~ -type f -size +20c -exec ls -hl {} \; - to find files over 20 bytes in size and list them out

find ~ -type f -size +20c -exec cp dir1 {} \; - locates all regular files within the user's home directory (and its subdirectories) that are larger than 20 bytes and then copies each of these files into a directory named dir1.

---

## Lesson 8:

### System and user details

uptime - finds out how long the system has been up and running

date - shows the current date and time

who - displays details about currently logged users

who -a - see other linux users

w - print the information about users who are currently logged into the system

mount - displays list of mounted file system

mount -t ext4 - view only ext4 file system

df -h - display free disk space on mounted devices

free -m - to find memory usage

---

## Lesson 9

### Linux Process Basic command

file /bin/hostname - shows the hostname

cat /bin/hostname - shows the instructions

ps - shows file on RAM

bash then ps - shows the parent process of a process

ps -o ppid 28578 - shows the parent of that process you get in the above command

ps -o ppid,cmd 31400 - shows the same thing as above but with the name of it

ps -o ppid,cmd 12781 - shows the parent of the primary Bach prompt (the number you got in the above command)

---

## Lesson 10

jobs - shows all background jobs

fg 5 - to bring job 5 to the foreground

press ctrl+z to stop the process

bg 5 to start the process correctly

---

## Lesson 11

seq 1 500000 - prints 1-500000 in the console

( ( kill -STOP 2498 ) ) - creates two more subshells and deletes the current one

( sleep 100 & ( kill -9 3329 )) - kills the subshell
