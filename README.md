# Hey! I'm Filing Here

This program makes a 1 MiB ext2 file system with 2 directories, 1 regular file containing the string "Hello World\n", and 1 symbolic link that points to that file, all within the root directory

## Building

To build, run the make command. 

## Running

After building, 
Show how to compile, mount, and example output of `ls -ain` your mounted
filesystem.

## Cleaning up

Explain briefly how to unmount the filesystem, remove the mount directory, and
clean up all binary files.


## Running

The code is compiled with the "make" command. Next, I made the directory "mnt" with the "mkdir mnt" command. Finally, I mounted the filesystem by first running "./ext2-create" followed by "sudo mount -o loop cs111-base.img mnt". The mounted filesystem can then be accesed with "cd mnt"

The command "ls -ain" gives the following output:

total 7
  2 drwxr-xr-x 3    0    0 1024 Mar 12 01:51 .
533 drwxr-xr-x 4 1000 1000 4096 Mar 12 01:55 ..
 13 lrw-r--r-- 1 1000 1000   11 Mar 12 01:51 hello -> hello-world
 12 -rw-r--r-- 1 1000 1000   12 Mar 12 01:51 hello-world
 11 drwxr-xr-x 2    0    0 1024 Mar 12 01:51 lost+found

## Cleaning up

To unmount the filesystem, the command "sudo umount mnt" is used. Then, I remove the mount directory with rmdir mnt. Lastly the binary files can be cleaned up with the "make clean" command.
