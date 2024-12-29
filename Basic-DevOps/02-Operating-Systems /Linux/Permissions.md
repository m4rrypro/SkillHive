# File and Directory Permissions
Understanding file and directory permissions is essential for managing access in Linux.

## Viewing Permissions
Use the `ls -l` command to view permissions:
ls -l

Example output:
-rw-r--r-- 1 user group 1234 Jan 1 12:00 example.txt

- `-rw-r--r--`: Represents the file permissions.
  - `r`: Read
  - `w`: Write
  - `x`: Execute

## Modifying Permissions
Change permissions using the `chmod` command:
chmod 755 filename

- `7`: Read, write, and execute
- `5`: Read and execute

## Changing Ownership
Use the `chown` command to change the ownership of a file:
chown user:group filename

## Practice Tasks
1. Create a file and modify its permissions to allow only the owner to read and write.
2. Create a directory and set its permissions to allow everyone to access it.
3. Change the ownership of a file to another user.
