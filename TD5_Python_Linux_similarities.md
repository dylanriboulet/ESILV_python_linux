# TD8/9: Linux, Git and Python

# Exercise 1: Working Directory

mkdir td4 && cd td4

git init

sudo apt-get install python3-pip

pip3 install virtualenv

virtualenv .env

source .env/bin/activate

pip list

git status

I created a .gitignore file with the following content:
.env/
__pycache__/
*.pyc
*.pyo
*.egg-info/
dist/
build/

git status

git add .gitignore && git commit -m "Initial commit"

# Exercice 2 Python Script

pip install requests


import requests

def fetch_place_ids(county_id):
    url = f"https://opendomesday.org/api/place/?county={county_id}"
    response = requests.get(url)
    data = response.json()
    return [place["id"] for place in data["results"]]

if __name__ == "__main__":
    derbyshire_id = 25
    place_ids = fetch_place_ids(derbyshire_id)
    print(place_ids)
    
 
    
 then I run fetch_place_ids.py
    

 git add fetch_place_ids.py && git commit -m "Add script to fetch place ids
 
 # Exericse 3: Python Module
 
 import requests

def get_manor_ids(place_id):
    url = f"https://opendomesday.org/api/manor/?place={place_id}"
    response = requests.get(url)
    data = response.json()
    return [manor["id"] for manor in data["results"]]

if __name__ == '__main__':
    # Replace PLACE_ID with the first place id from Derbyshire
    PLACE_ID = 'PLACE_ID'
    manor_ids = get_manor_ids(PLACE_ID)
    print(manor_ids)
    
    
then I run manors.py


git add manors.py && git commit -m "Add Python module to get manor ids

