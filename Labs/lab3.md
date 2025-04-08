## Create a user account with the following attribute
   • username: “your first name”
   • Fullname/comment: “full name”
   • Password: islam

  ```
sudo useradd -c "Ahmed Magdy" -m ahmed

```
![Screenshot 2025-04-07 141537](https://github.com/user-attachments/assets/1a7345bd-f5ad-4806-b3c3-c970db5042cb)
![Screenshot 2025-04-07 141558](https://github.com/user-attachments/assets/4de0e315-6205-40b4-b6f8-2e73a8a19722)

## 2. Create a user account with the following attribute
   • Username: baduser
   • Full name/comment: Bad User
   • Password: baduser

   ```
   sudo useradd -c "Bad User" -m baduser
   sudo passwd baduser
   
   ```
![image](https://github.com/user-attachments/assets/e9938198-a01a-4101-8556-75c61feaed00)


## 3. Create a supplementary (Secondary) group called pgroup with group ID of 30000

```
sudo groupadd -g 30000 sgroup

```
## 4. Create a supplementary group called badgroup
```

sudo groupadd badgroup

```

![image](https://github.com/user-attachments/assets/9ee6ede2-09ca-4f99-a8dc-eb0110ffd5cd)

## 5. Add  user to the pgroup group as a supplementary group
```

sudo usermod -aG sgroup ahmed

```
## 6. Modify the password of  account to password
```

sudo passwd ahmed

```
![image](https://github.com/user-attachments/assets/a10906ff-3eae-4336-85c1-15af627dc668)


## 7. Modify account so the password expires after 30 days
```
sudo chage -M 30 ahmed
sudo chage -l ahmed
```
![image](https://github.com/user-attachments/assets/ca6876a3-67d3-40b1-9003-56f553f97f0f)


## 8. Lock bad user account so he can't log in
```
sudo usermod -L baduser

```
## 9. Delete bad user account
```
sudo userdel -r baduser

```
## 10. Delete the supplementary group called badgroup

```
sudo groupdel badgroup

```
### 11. Create a folder called myteam in your home directory and change its permissions to read only for the owner.
12. Log out and log in by another user
13. Try to access (by cd command) the folder (myteam)
14. Using the command Line
    • Change the permissions of oldpasswd file to give owner read and write permissions and for group write and execute and execute only for the others (using chmod in 2 different ways)
    ```
    chmod u+rw,g+wx,o+x oldpasswd
    chmod 631 oldpasswd
    ```
    • Change your default permissions to be as above.
    ```
    setfacl -Rdm u::rw-,g::-wx,o::--x /home
    
    ```
    ![image](https://github.com/user-attachments/assets/d9b9fcd9-9a5c-428a-92a3-b1ab6709cae9)

    • What is the maximum permission a file can have, by default when it is just created? And what is that for directory.

    Files: When an application creates a new file, it typically requests a maximum permission of 666 (rw-rw-rw-). This means read and write permissions for the owner, group, and others.
    Directories: When an application creates a new directory, it typically requests a maximum permission of 777 (rwxrwxrwx). This means read, write, and execute permissions for the owner, group, and others.

     • Change your default permissions to be no permission to everyone then create a directory and a file to verify.
    ```
    setfacl -Rdm u::---,g::---,o::--- /home

    ```
    
## 15. Starting from your home directory, find all files that were modified in the last two day.
```
find -type f -mtime -2
```
![image](https://github.com/user-attachments/assets/931cff8f-8f40-4807-88fb-8258ba417aae)

## 16. Starting from /etc, find files owned by root user.
```
find /etc -user root

```
![Screenshot 2025-04-07 152958](https://github.com/user-attachments/assets/1f68f12e-f2fe-4c1f-a9c6-3e42c7c140b5)


## 17. Find all directories in your home directory.
```
find  -type d

```
![Screenshot 2025-04-07 153042](https://github.com/user-attachments/assets/e5a839ab-9908-43fb-bf4a-183bed76d8dd)

## 18. Write a command to search for all files on the system that, its name is ".profile".

```
find / -type f -name ".profile"

```
![Screenshot 2025-04-07 153436](https://github.com/user-attachments/assets/2a21c604-b49c-4bbc-a993-7034ba8a0134)

## 19. Identify the file types of the following: /etc/passwd, /dev/pts/0, /etc, /dev/sda
```
file /etc/passwd
file /dev/pts/0
file /dev/sda
file /etc
```
![image](https://github.com/user-attachments/assets/8fffff33-06f5-434f-b404-4a613ac33375)

## 20. List the inode numbers of /, /etc, /etc/hosts.
```
ls -id /
ls -id /etc/
ls -id /etc/hosts

```

![image](https://github.com/user-attachments/assets/62b47334-430b-4d8f-a173-6405f11f1bdf)

## 21. Copy /etc/passwd to your home directory, use the commands diff and cmp, and Edit in the file you copied, and then use these commands again, and check the output.

```
sudo cp /etc/passwd /home/cpasswd
sudo diff /etc/passwd  passwd
sudo cmp /etc/passwd passwd
sudo nano passwd
sudo diff /etc/passwd  passwd
sudo cmp /etc/passwd passwd

```

![image](https://github.com/user-attachments/assets/ca101204-9752-4ea8-88a6-2bea72ff4245)

![image](https://github.com/user-attachments/assets/a44c17d2-6ab3-477f-9962-f2ee60184fbd)


## 22. Create a symbolic link of /etc/passwd in /boot.
```
sudo ln -s /etc/passwd /boot/passwd_slink
```
    
## 23Create a hard link of /etc/passwd in /boot. Could you? Why?
```
sudo ln /etc/passwd /boot/passwd_hlink

```

![Screenshot 2025-04-08 235815](https://github.com/user-attachments/assets/c626c6dd-9aac-4d95-8b23-6a16b46d5745)

