# Lab 1 
## What is the difference between cat and more command?
**cat:** Displays the entire content of a file all at once, regardless of the file's length. You might need to scroll up to view earlier parts of the content 

**more:** The more command allows viewing the contents of a file by one screen at a time. That means it stops displaying when it fills one screen

## What is the difference between rm and rmdir using man?

The **rm** command is a versatile tool used to delete files and directories. It can remove both empty and non-empty directories, as well as individual files

The **rmdir** command is specifically designed to remove empty directories. It cannot remove directories that contain files or other directories.

## Create the following hierarchy under your home directory:
![image](https://github.com/user-attachments/assets/21bdbe7d-9664-48ed-9428-d72375c929b8)

```
 Mkdir dir1
 Mkdir  dir1/dir11
 Mkdir dir1/dir12
 Touch dir1/dir/11/file1
 Mkdir docs 
 Touch docs/mycv
```
![Screenshot 2025-04-05 212836](https://github.com/user-attachments/assets/4f4aa46c-4b44-4cb2-a10a-b6f699ce9e47)
![Screenshot 2025-04-05 212933](https://github.com/user-attachments/assets/8db1007b-866f-405d-a228-60c7917fd05d)

* a) Remove dir11 in one-step
```
rm -r dir1/dir11

```


* b) Then remove dir12 using rmdir –p command. State what happened to the
hierarchy

```
rmdir -p dir1/dir12

```
   the dir12 is deleted and using the -p option the parent directory is deleted becauese it's empty 

* c) The output of the command pwd was /home/user. Write the absolute
and relative path for the file mycv

**relative path** : /docs/mycv

**absolute path** :  home/vboxuser/mycv

## Copy the /etc/passwd file to your home directory making its name is mypasswd.

```
cp /etc/passwd  mypasswd

```

## Rename this new file to be oldpasswd.

```
mv mypasswd  old passwd

```
## You are in /usr/bin, list four ways to go to your home directory

```
cd 
Cd /home/vboxuser
Cd ~
cd-
cd $Home

```
## List Linux commands in /usr/bin that start with letter w
```
cd /usr/bin
Ls | grep ‘^w’

```
![Screenshot 2025-04-05 154311](https://github.com/user-attachments/assets/0a67a5e5-41c0-4dd5-8811-f1e6853a1312)

## Display the first 4 lines of /etc/passwd
```
head -n 4 /etc/passwd

```
## Display the last 7 lines of /etc/passwd

```
tail -n 7  /etc/passwd

```
![Screenshot 2025-04-05 200930](https://github.com/user-attachments/assets/9e341a3d-7669-4917-8dd3-333d8ee3f42b)

##  Display the man pages of passwd the command and the file sequentially in one command.

```
man 1 passwd && man 5 passwd

```
![Screenshot 2025-04-05 201519](https://github.com/user-attachments/assets/62c48263-da93-4cfb-ae5e-bbae4105dfe3)
![Screenshot 2025-04-05 201536](https://github.com/user-attachments/assets/2fdefe9d-15d8-4a90-b735-1d4923b8bb7f)

## Display the man page of the passwd file.

```
man 5 passwd

```
## Display a list of all the commands that contain the keyword passwd in their man page.

```
man -k passwd

```

![Screenshot 2025-04-05 202847](https://github.com/user-attachments/assets/3af2b054-00ca-4652-817e-463d002a06f2)

## Using vi write your CV in the file mycv. Your CV should include your name, age, school,
college, experience,...


![Screenshot 2025-04-05 205240](https://github.com/user-attachments/assets/09da03cf-d56e-441e-a73c-030fd8230840)

* Open mycv file using vi command then: Without using arrows state how to:
  
  ```
  vi mycv
  ```
1. Move the cursor down one line at time.
   
    j
1. Move the cursor up one line at time.
   
    k
1. Search for word age

   :/age

1. Step to line 5 (assuming that you are in line 1 and file is more than 5 lines).

   5 + enter
1. Delete the line you are on and line 5.
    dd
1. How to step to the end of line and change to writing mode in one-step.
   A

## st the available shells in your system.
```
cat /etc/shells

```
![Screenshot 2025-04-05 221318](https://github.com/user-attachments/assets/d05afeef-8303-4d30-bfae-ca2182ce2145)



