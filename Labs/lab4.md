## 1. List **all running processes** and save the output to `~/processes.txt`.  
```
ps aux > ~/processes.txt

```
![Screenshot 2025-04-08 141743](https://github.com/user-attachments/assets/361f8875-35f3-4e3c-9695-69ec00639878)


## 2. Find the **PID (Process ID)** of the `sshd` service.
```
ps aux | grep 'sshd'

```
![Screenshot 2025-04-08 143655](https://github.com/user-attachments/assets/c55600d0-d504-4196-8277-4ab177635a74)

   
3. Run a `sleep 500` command in the background, then **kill it** after 5 seconds.  

```
sleep 500 & pid=$!
sleep 5
kill $pid

```
![Screenshot 2025-04-08 144350](https://github.com/user-attachments/assets/00993393-422b-4b6a-a889-dd673bb84ccc)


## 4. Install `apache2` service, edit the default HTML file (`/var/www/html/index.html`), and verify changes in a web browser.
```
sudo apt install apache2
nano /var/www/html/index.html

```
![Screenshot 2025-04-08 145259](https://github.com/user-attachments/assets/fe5d95cf-b4e8-401b-b362-5600f7ec09d6)

![Screenshot 2025-04-08 145321](https://github.com/user-attachments/assets/aba5263b-dc2e-48f6-870d-03c0cdbd9afe)

![Screenshot 2025-04-08 145340](https://github.com/user-attachments/assets/77a06b5a-d270-43df-82e0-c7279dd59b69)


## 5. **Check if `sshd` (SSH service) is running**. If not, start and enable it.  
```
sudo systemctl status ssh
sudo systemctl start ssh

```
![Screenshot 2025-04-08 145800](https://github.com/user-attachments/assets/cb9e1b60-cdd9-4b27-9ec2-ec77ae9bbe67)

![Screenshot 2025-04-08 145809](https://github.com/user-attachments/assets/a386eb30-14da-4eee-9de5-fa4273ccd405)

## 6. **Restart the `cron` service** and verify its status.  
```
sudo systemctl restart cron
sudo systemctl status cron

```
![Screenshot 2025-04-08 150002](https://github.com/user-attachments/assets/93fdd36d-72a6-4724-af43-94f6b3c76aa9)

## 7. Create a **compressed tarball** (`archive.tar.gz`) of `/var/log` and save it in your home directory. 
```
sudo tar -czvf ~/archive.tar.gz  /var/log

```

![Screenshot 2025-04-08 150234](https://github.com/user-attachments/assets/b0ee6f2c-0d3f-44e0-9895-72da100ab79a)

## 8. **Extract** the tarball into `~/logs_backup/`.  
```
sudo tar -xzvf ~/archive.tar.gz .c ~/logs_backup

```

![Screenshot 2025-04-08 150823](https://github.com/user-attachments/assets/50685b86-b4a5-4644-b0dc-3de341296d49)


## 9. Create a **non-compressed tarball** (`archive.tar`) of `/etc/ssh` and save it in `/tmp`. 
```
sudo tar -cvf /tmp/archive.tar /etc/ssh

```
![Screenshot 2025-04-08 151607](https://github.com/user-attachments/assets/75f47a54-9685-4a39-b038-259c670ee55a)

## 10. Compress `~/processes.txt` using `gzip`.  
## 11. **Decompress** it and compare file sizes using `ls -lh`.  
```
gzip ~/processes.txt
ls -lh ~/processes.txt.gz
gzip -d ~/processes.txt.gz
ls -lh ~/processes.txt

```
![image](https://github.com/user-attachments/assets/ed864c8f-fe65-4846-b140-655729d6462f)

## 12. **Install `htop`** (a process viewer) using your package manager.  
```
sudo apt install htop -y

```
![image](https://github.com/user-attachments/assets/a1b540ed-45b6-458e-b8be-91255f30ad58)

## 13. **Search for the package `nginx`** (or `httpd`) but do not install it.  
```
apt search nginx
apt search httpd
```
![image](https://github.com/user-attachments/assets/56ae961c-74b3-4885-86c8-e45adbcfa958)

## 14. **Remove the `vim` editor** (if installed) and then reinstall it.  
```
sudo apt remove vim
sudo apt install vim
```

![image](https://github.com/user-attachments/assets/3b9e27ed-2a42-44e4-9c8e-88985ac7f3cc)

15. Use `wget` to download the Linux kernel source:  
```
wget https://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.8.1.tar.xz

```    

![image](https://github.com/user-attachments/assets/6e97348f-7e15-41da-b3e2-0bf107b5abb8)

16. Use `curl` to fetch **Google’s homepage** and save it as `google.html`.  
```
curl https://www.google.com -o google.html
```
![image](https://github.com/user-attachments/assets/13423aca-2fe6-495f-b277-7458d62c39e3)

## 17. **Create a new VM** (e.g., VirtualBox/Cloud instance), add a user to the `sudoers` group, and run `apt update && apt upgrade`.  

## 18. **Generate an SSH key pair** using `ssh-keygen`.  
## 19. **Copy your public key** to the remote server:  
## 20. **SSH into the server** and verify with `hostname`.  
## 21. **Transfer the archived file** (e.g., `archive.tar.gz`) to the remote server using ssh copy way (don’t copy/paste >>> you have to search)

