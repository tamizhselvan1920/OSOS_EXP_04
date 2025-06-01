# Exp 4 : Create a collaborative directory 

# AIM:
To create a collaborative directory

# EQUIPMENTS REQUIRED:
Hardware: Minimum 4 GB RAM and 25 GB storage – essential for running services like Cockpit and handling system updates smoothly.
Software: Red Hat Enterprise Linux (RHEL) or any open-source Linux OS like Fedora or CentOS Stream – used for system administration and repository creation.

# PROCEDURE & COMMENTS:

1. Creating a directory 
The first line [root@servera ~]# mkdir -p /common/admin creates a new 
directory named /common/admin. The mkdir command is used to create new directories. 
The -p option tells mkdir to create any parent directories that do not already exist. For example, 
if the directory /common did not exist, the -p option would create it automatically. 
2. Changing directory ownership 
The line [root@servera ~]# chgrp admin /common/admin changes the group 
ownership of the directory /common/admin to the group admin. The chgrp command is 
used to change the group ownership of a file or directory. In this case, the directory /common/
admin is given ownership by the admin group, which was likely created earlier. 
3. Changing directory permissions 
The line [root@servera ~]# chmod 770 /common/admin changes the permissions 
of the directory /common/admin. The chmod command is used to change the permissions of 
a file or directory. There are three sets of permissions: read, write, and execute. Each set of 
permissions applies to the owner of the file, the group that owns the file, and all other users on the 
system. 
In this case, the command sets the following permissions for /common/admin: 
• The owner (root) can read, write, and execute the directory (7). 
• The admin group can read, write, and execute the directory (7). 
• All other users cannot access the directory (0). 
4. Setting a sticky bit 
The line [root@servera ~]# chmod g+s /common/admin/ sets the sticky bit on 
the directory /common/admin. The sticky bit is a special permission that affects how files 
within the directory are deleted. When set, only the owner of the file or the root user can delete 
the file, regardless of the write permissions for the directory. 
5. Viewing directory permissions 
7
The line [root@servera ~]# ls -ld /common/admin lists the details of the 
directory /common/admin. The ls command is used to list files and directories. The -l option 
shows detailed information about the files, including permissions. The -d option specifies that 
only directory information should be listed. 
The output drwxrws. 2 root admin 6 May 7 14:19 /common/admin shows 
the following details about the directory: 
• d: This indicates that it is a directory. 
• rwx: The owner (root) has read, write, and execute permissions. 
• rws: The admin group has read, write, and execute permissions. 
• .: There is no special permission for other users (no read, write, or execute). 
• 2: This is the number of hard links to the directory. 
• root: This is the owner of the directory. 
• admin: This is the group that owns the directory. 
• 6: This is the size of the directory in bytes (usually 0 bytes for directories). 
• May 7 14:19: This is the date and time the directory was last modified. 
• /common/admin: This is the name of the directory. 
6. Switching to a different user 
The line [root@servera ~]# su - harry switches the user from root to the user 
harry. The su command is used to switch users on a Linux system. The - option tells su to start 
a new login shell for the specified user. 
7. Creating a file 
The line [harry@servera ~]$ touch /common/admin/file1 creates a new file 
named file1 inside the directory /common/admin. The touch command is used to create 
a new empty file. 
8. Viewing file permissions 
The line [harry@servera ~]$ ls -l /common/admin/file1 lists the details of 
the file /common/admin/file1. The same options used with the ls command previously 
are used here to show detailed information about the file, including permissions. 
The output -rw-r--r-- 1 harry admin 0 May 7 23:39 /common/admin/file1 shows the following details.

# EXPECTED OUTPUT


![Screenshot 2025-06-01 144119](https://github.com/user-attachments/assets/4a1e7c31-ac6a-4014-8ba2-8394dfa519b4)

# RESULT:
Thus a collaborative directory has been created successfully.. 
