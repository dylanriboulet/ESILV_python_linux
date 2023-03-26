
# Here the commands I used on my Git Bash using history

# Exercice 1:

git --version

git config --global user.name "dylanriboulet"

git config --global user.email "dylan.riboulet@gmail.com"

git config --list

# Exercice 2:

git init

ls -la

git status

echo "# Test repository" > readme.md

git status

git add readme.md

git status

git commit -m "Add readme.md"

git status

git log

# Exercice 3:

touch main.py functions.py

git status

git add main.py

git status

git commit -m "Add main.py"

git status

git add functions.py

git commit -m "Add functions.py"

git status

git log


# Exercice 4

touch requirements.txt .gitignore .private

git status

git status

git commit -m "Add required files"

git status

git log --oneline

touch temp.ipynb

temp.ipynb

echo "temp.ipynb" >> .gitignore

git status

touch temp.aux temp.log

echo "temp*" > .gitignore

git status

# Exerice 6:

git add readme.md

git diff --cached

git commit -m "Update readme.md with description"

git diff

git diff HEAD^

git diff

# Exericice 7:

rm *

git restore .

cp -r .git /path/to/backup

rm -rf * && cp -r /path/to/backup/.git . && git restore .

git restore --staged readme.md

git commit -a -m "Direct commit without staging"

git log

git checkout HEAD~1

git log

git log --all

git checkout -

git revert HEAD

ls

git log

git reset --hard HEAD~2

ls

git log

# Exercice 8

git config --global alias.s status

git config --global alias.co checkout

git config --global alias.b branch

git config --global alias.ci commit

git config --global alias.dog "log --all --decorate --oneline --graph"

git config --global alias.dag "log --all --decorate --graph"

git config --global alias.list "diff-tree --no-commit-id --name-only -r"

git config --global alias.unstage "reset HEAD --

git config --global alias.last "log -1 HEAD"

# Exercice 9

mkdir root-directory && cd root-directory

echo "Hello World" > hello.txt

wc -c hello.txt

cat hello.txt

sha1sum hello.txt

git hash-object hello.txt

echo -e "blob 11\0Hello World" > hello_modified.txt

sha1sum hello_modified.txt

# Exercice 10

git init

git status

ls .git/objects

mkdir -p .git/objects/first_two_characters_of_hash

sudo apt-get install qpdf

zlib-flate -compress < hello_modified.txt > .git/objects/first_two_characters_of_hash/last_38_characters_of_hash

git cat-file -t hash_object and git cat-file -p hash_object
