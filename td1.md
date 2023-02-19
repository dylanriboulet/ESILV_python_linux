# TD1: Use basic Linux commands

## Exericice 1

1.  Go to the root directory
```
cd /
```
cd signifie change directory et / représente le root directory

2.  Display the content of the current (root) directory
```
ls -a
```

3. Check your current location
```
pwd
```

4.  Try to create a directory named test
```
mkdir test
```
output: cannot create directory ‘test’: Permission denied

5.  Go to the general home directory (should contain folders named after
each user)
```
cd /home
```

6.  Go to your home directory
```
cd 
cd ~
```
Les deux commandes précédentes sont équivalentes
Cela revient à faire cd /home/dylanriboulet

7. Go back to the general home directory (located "just above")
```
cd ..
```

8. retourner en arrière
```
cd ..
```
pour remonter au fichier qui est juste au dessus
permet de remonter jusqu'à la racine

9. Go directly to your home directory (named after you). It should be a
very simple command, which take no name as parameter of the path
```
cd
```

10. Try to create a directory named test
```
mkdir test
```
Commentaire : pas de messages en sortie

11. Go into this new directory
```
cd test
```

12. Check your current location
```
pwd
```
output: /home/dylanriboulet/test

## Exercise 2: Create, Rename, copy, delete

1. Go to your home directory (should be named after you, you might be
there by default)
```
cd
```

2. Check your current location
```
pwd
```
Output: /home/dylanriboulet

3.  Create a folder linux_ex_1
```
mkdir linux_ex_1
```

4. Go into this folder
```
cd linux_ex_1
```

5. Create an empty text file named [first_name]_[last_name].txt
```
vim dylan_riboulet.txt
```

6. Create a folder notes
```
mkdir notes
```

7. Move your text file into this folder
```
mv dylan_riboulet.txt notes/
```

8. Rename the text file by appending the current year [first_name]_[last_name]_[current_year].txt
```
mv dylan_riboulet.txt dylan_riboulet_2023.txt
```

9. Make a copy of this folder, name it notes_2022
```
cp -r notes notes_2022
```

10. Delete the first folder (notes) using the verbose option
```
rm -rv notes
```
v est la verbose option (donne davantages de détails sur ce que l'on fait)


## Exercise 3: Create and run a script

1. Create a script script_1.sh in the folder linux_ex_1
```
vim script_1.sh
```

2. In the script, write the commands that would output the following :
Script running please wait ...
Done.
```
#!/bin/bash

echo "Script running please wait ..."
echo "Done."
```
commentaire: en utilisant le mode écriture i

3. Quit editing and save the script
Echat -> sortir du mode écriture (commande i sur clavier) \n
:w -> enregistrer le script \n
:q -> sortir du script \n
:wq -> enregistrer et quitter le script \n

4. Display the content of the script (using a command, not from an editor)
```
cat script_1.sh
```

5. Run the script
```
source script_1.sh
```
ou 
```
bash script_1.sh
```

## Exercise 4: Accessing or modifying a file : permissions and root privilege

### Exercise 4:.1 Change the rights for accessing or modifying a file

1. Create a file credentials in the folder linux_ex_1
```
vim credentials
```

(a) Write any kind of (fake) personal information within the file
This will open the vim text editor. Type in some fake personal information, and then save and exit the file by typing :wq and pressing Enter.


(b) Display the file content
```
cat credentials
```

(c) Display the current permissions
```
ls -l credentials
```
output: -rw-r--r-- 1 dylanriboulet dylanriboulet 11 Feb 19 02:16 credentials

2. Change the current permissions to : read only for all users
```
chmod a-w credentials
```

(a) Display the new permissions
```
ls -l credentials
```
output: -r--r--r-- 1 dylanriboulet dylanriboulet 11 Feb 19 02:16 credentials

(b) Modify and save the file
```
vim credentials
```

(c) Display the file content
```
cat credentials
```

3. Change the permissions back to read and write for all users
```
chmod a+rw credentials
```

(a) Display the new permissions
```
ls -l credentials
```
output: -rw-rw-rw- 1 dylanriboulet dylanriboulet 11 Feb 19 02:16 credentials

(b) Modify and save the file
```
vim credentials
```

(c) Display the file content
```
cat credentials
```

1. Add the execute permission to the owner
```
chmod u+x credentials
```

(a) Display the new permissions
```
ls -l credentials
```
output: -rwxrw-rw- 1 dylanriboulet dylanriboulet 11 Feb 19 02:16 credentials

2. Remove the read permission to other users
```
chmod o-r credentials
```

(a) Display the new permissions
```
ls -l credentials
```
output: -rwxrw--w- 1 dylanriboulet dylanriboulet 11 Feb 19 02:16 credentials

3. Change the permissions to read, write and execute for all users
```
chmod a=rwx credentials
```

(a) Display the new permissions
```
ls -l credentials
```
output: -rwxrwxrwx 1 dylanriboulet dylanriboulet 11 Feb 19 02:16 credentials


### Exercise 4:.2 Access root files

1. Go to the root folder
```
sudo su -
```

2. Create a file in root user mode named .private_file
```
touch .private_file
```

(a) Write some information in the file
```
sudo vim .private_file
```

(b) Display the file content
```
sudo cat .private_file
```

3. Modify the file in normal user mode
```
vim .private_file
```

(a) Write some new information in the file
i
write something
:wq

(b) Display the file content
```
cat .private_file
```

4. Modify the file in root user mode
```
sudo vim .private_file
```

(a) Write some new information in the file
i
write something
:wq

(b) Display the file content
```
sudo cat .private_file
```

5. Change permissions to read, write and execute for all users
```
sudo chmod 777 .private_file
```

(a) Modify the file content in normal user mode
```
vim .private_file
```

(b) Display the file content
```
cat .private_file
```

### Exercise 4:.3 Change a file owner

1. Change permissions of .private_file to read and write for all users, in
normal user mode
```
chmod a+rw .private_file
```

2. Set the new file owner as the current user
```
sudo chown $USER .private_file
```

3. Change permissions of .private_file to read and write for all users, in
normal user mode
```
chmod a+rw .private_file
```

### Exercise 4:.4 Manage Packages (tools / functions)

1. Update your main package manager named apt
```
sudo apt update
```

2. Upgrade apt
```
sudo apt upgrade
```

3. Install the package cmatrix
```
sudo apt install cmatrix
```

4. Launch cmatrix
```
cmatrix
```

5. Quit cmatrix
Ctrl + C

6. Install the package tmux
```
sudo apt install tmux
```

7. Launch tmux
```
tmux
```

8. Say "Hello session 0" using bash in your current tmux session
```
echo "Hello session 0"
```

9. Launch cmatrix in your current tmux session
```
cmatrix
```

10. Detach from the current tmux session (without stopping cmatrix)
Ctrl + B
puis d

11. Create a new tmux session
```
tmux new -s mysession
```

12. Say "Hello session 1" using bash in your new tmux session
```
echo "Hello session 1"
```

13. Detach from the current tmux session
Ctrl + B
puis d

14. List all running sessions
```
tmux ls
```

15. Attach again to session 0
```
tmux attach-session -t 0
```

16. Detach again
Ctrl + B
puis d

17. Attach again to session 1
```
tmux attach-session -t mysession
```

18. Detach again
Ctrl + B
puis d

19. List all running sessions
```
tmux ls
```

20. Kill all tmux sessions and quit tmux
```
tmux kill-server
```

21. List all sessions
```
tmux ls
```
output: no server running on /tmp/tmux-1000/default


### Exercise 4:.5 Use functions arguments / parameters
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

il y a rien qui va de au de la racine 
root
il y a la racine 
il y a home et basta



```
ls -a
```
h
```
ls -a
```
