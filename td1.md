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
