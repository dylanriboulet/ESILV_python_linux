# TD2: Fundamental Linux functionalities

## Exercise 1: Access general computer informations

1. Put system up to date
```
sudo apt update
sudo apt upgrade
```

2. Display
Linux version
```
uname -a
```

Current processes and memory usage associated
```
top
```

Display it in a more pleasant way ("more readable for humans")
```
htop
```

Number of processors
```
nproc
```

L1, L2 and L3 cache size
```
lscpu | grep -E 'L1d|L1i|L2|L3'
```

Disk space
```
df -h
```

Monted devices
```
mount
```

Connected usb devices
```
lsusb
```

Hostname
```
hostname
```

## Exercise 2: Shell - Variables and scripts scope

1. Create a variable x and assign it the short text piri pimpin
```
x="piri pimpin"
```

2. Display the value of this variable
```
echo $x
```

3. Add to this value the following text piri pimpon
It should contain the following : piri pimpim piri pimpon
```
x+=" piri pimpon"
echo $x
```
output piri pimpin piri pimpon

4. Create a folder named my_programs, then enter into that folder
```
mkdir my_programs
cd my_programs
```

5. Create a script named pilou that displays pilou pilou
```
echo "pilou pilou" > pilou
```

6. Run this script
```
cat pilou
```

7. Make this script executable
```
chmod +x pilou
```

8. Run the script by writting its name only
```
./pilou
```

9. Programs called from the terminal are usually found thanks to a variable
named PATH
Display the content of the variable PATH
```
echo $PATH
```

10. Add the path of your current location to the global variable PATH
```
PATH=$PATH:/path/to/current/location
```

11. When you are sure of the result, export it
```
export PATH
```

12. Go to your home directory
```
cd ~
```

13. Run your script by writting its name only
```
pilou
```

14. Change the value of the PATH in the .profile file in order to make it
permanent
```
PATH=$PATH:/path/to/my_programs
```

15. Create a new shell and run your script using its name only
```
pilou
```
En ouvrant une nouvelle fenetre terminale 

## Exercise 3: Scheduling task - daemon

1. Create a script say_hello.sh
```
mkdir say_hello.sh
```

```
echo "$(date) Hello" >> hellos.txt
```

2. Make the script executable
```
chmod +x say_hello.sh
```

3. Use crontab to schedule the running of the script every minute
```
crontab -e
* * * * * /say_hello.sh
```


## Exercise 4: Hashing

1. Create a folder named hash_checksum. Go into this folder
```
mkdir hash_checksum
cd hash_checksum
```

2. Inside this folder, create two files named .sensible_addresses and .sensible_passwords
```
touch .sensible_addresses
touch .sensible_passwords
```

3. Display the list of files of the folder
```
ls -a
```

4. Still inside the folder hash_checksum, create a script named gentle_script.sh.
This script should display the following text "Have a good day"
```
echo "Have a good day" > gentle_script.sh
```

5. Run the script
```
bash gentle_script.sh
```

6. Compute the sha256sum of gentle_script. Store it into a file named
log_sha
```
sha256sum gentle_script.sh > log_sha
```

7. Now corrupt the file by adding a line of code that deletes any file starting
with : ".sensible"
```
echo "rm -rf .sensible*" >> gentle_script.sh
```

8. Compute again the sha256sum of gentle_script. Store it into the log_sha
file
```
sha256sum gentle_script.sh >> log_sha
```

9. Run the script
```
bash gentle_script.sh
```

10. Display again the list of files of the folder
```
ls -a
```

11. Display the log_sha content : are the hashes any different ?
```
cat log_sha
```

## Exercise 5: Compressing

1. Install the QPDF free command-line program.
Part of this program is the zlib-flate command that compress and uncompress files using the deflate algorithm.
```
sudo apt-get install qpdf
```

2. Create a directory "compress", go into this directory
```
mkdir compress
cd compress
```

3. Create a first file "hello" whose content is "Hello"
```
echo "Hello" > hello
```

4. Compute the deflate compression (level 1) of this file. Store the compressed file size into a file log_compress
```
zlib-flate -1 < hello | wc -c > log_compress
```

5. Create a second file "hello_multiple" whose content is 1000 lines of "Hello"
```
yes "Hello" | head -n 1000 > hello_multiple
```

6. Compute the deflate compression (level 1) of this file. Store the compressed file size into a file log_compress
```
zlib-flate -1 < hello_multiple | wc -c >> log_compress
```

7. Create a third file "hello_mulitple_i" whose content is 1000 lines of "Hello
i" (i varying from 1 to 100)
```
for i in {1..100}; do echo "Hello $i"; done > hello_multiple_i
```

8. Compute the deflate compression (level 1) of this third file. Store the
compressed file size into log_compress
```
zlib-flate -1 < hello_multiple_i | wc -c >> log_compress
```

9. Display the content of log_compress
```
cat log_compress
```

10. Compute the compression ratio of each file, also display it as a simple
fraction (e.g. 12.6 => 10 :1)
```
echo "Compression ratio:"
echo "Hello: $(echo "$(stat -c%s hello_compressed) / $(stat -c%s hello)" | bc | factor)"
echo "Hello_multiple: $(echo "$(stat -c%s hello_multiple_compressed) / $(stat -c%s hello_multiple)" | bc | factor)"
echo "Hello_multiple_i: $(echo "$(stat -c%s hello_multiple_i_compressed) / $(stat -c%s hello_multiple_i)" | bc | factor)"
```

11. Analyse the results
On constate que le taux de compression diminue à mesure que le fichier devient plus complexe.


## Exercise 6: ACLs : Access Control Lists
```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

```

