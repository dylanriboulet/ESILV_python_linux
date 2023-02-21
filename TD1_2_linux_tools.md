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

