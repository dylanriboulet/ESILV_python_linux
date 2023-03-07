
## TD4/9: Work with secured distant communication tools

# Exercise 1: SSH

4. Create a script named connect.sh to automatically connect to the remote
instance
```
#!/bin/bash

ssh -i path/to/private_key.pem dylanriboulet@74.234.17.109
```

5. Run the script to check it is working properly. Then exit to return to
your local machine
To run the script, we need to make it executable using the chmod command:
Then we can run the script
```
chmod +x connect.sh
./connect.sh
```


# Exercise 2: SCP
```
> test_to_remote_instance.txt
```

```
To send our file to the remote instance: 
```
scp -i path/to/private_key.pem test_to_remote_instance.txt user@remote_instance_ip:~

```
To get the file from the remote instance:
```
scp -i path/to/private_key.pem user@remote_instance_ip:test_from_remote_instance.txt .
```

```
