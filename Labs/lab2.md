# lab2

## List the available shells in your system.
```
cat /etc/shells
```
![Screenshot 2025-04-05 221302](https://github.com/user-attachments/assets/847c248d-c391-4d31-b5b2-abd5e9521b33)

## List all of the environment variables in your current shell.
```
compgen -v

```
![Screenshot 2025-04-06 152945](https://github.com/user-attachments/assets/60b008bc-45c5-410d-a12a-dfdb295a0999)

## Display your current shell name.
```
echo $SHELL

```
![Screenshot 2025-04-06 135224](https://github.com/user-attachments/assets/b4dd801d-e8df-4162-a577-d00a1cd446bf)


## List all of the environment variables for the Bash shell.
```
printenv

```
![Screenshot 2025-04-06 135119](https://github.com/user-attachments/assets/35fee854-7b00-412e-93f8-a6f3e01aa798)

## Edit your shell profile to display the date at login and change your prompt.
```

```
![Screenshot 2025-04-06 140600](https://github.com/user-attachments/assets/ab7ca97c-97a2-49d3-9866-71ddd88e632e)
![Screenshot 2025-04-06 140628](https://github.com/user-attachments/assets/5dd12ef2-dc6f-414e-8e6a-325bb4596948)

## Redirect the output of the ls command to a file called file_list.txt.
```
ls > files_list.txt
```
![Screenshot 2025-04-06 140834](https://github.com/user-attachments/assets/7ca90d8f-9c7d-4aee-9043-57aef08a724a)

## Use file globbing to list all .txt files in the current directory.
```
ls *.txt

```

![Screenshot 2025-04-06 141325](https://github.com/user-attachments/assets/6afc8334-053a-4158-bd4f-14f907f555d6)

## Redirect the output of the ls command to a file and append it.
```
ls >> files_list.txt

```

## Use a pipe to send the output of ls to the grep command to filter for files containing the word "report".
```
ls -LR | grep "report"
```
![Screenshot 2025-04-06 150946](https://github.com/user-attachments/assets/f1588d8b-870e-4c7e-af97-2194bd71d3f7)

## Use head to view the first 10 lines of a file, and tail to view the last 10 lines.
```

```
## Use cut to extract the second column of a file called data.csv.
```

```
## Search for all lines in a file called log.txt that contain the word "ERROR" using grep.
```

```
## Create a shell variable called current_user to store the output of the whoami command.
```

```
## Use tr to convert a string of lowercase letters to uppercase.
```

```
## Use a pipe to send the output of ps to grep to search for a specific process name.
```

```
## Create a Bash alias named ls for the command ls -l.
```

```
## Use sort to sort the output of ls -l by file size.
```

```
## Use grep to count the number of lines that contain the word "success" in a file.
```

```
## Redirect the output of the dmesg command to a file and view the first 20 lines using head.
## Use cut to extract the first field from a CSV file and display it.


