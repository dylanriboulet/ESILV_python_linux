
# TD3: Work with text manipulation tools in Linux

## Exercise 1: Access general computer informations

1. Display the list of files and folders at the root using ls -l
```
ls -l
```

2. In a pipeline (using |), append a grep instruction to only display informations of bin
```
ls -l | grep bin
```

3. Append an awk instruction to only display the size of bin
```
ls -l / | grep bin | awk '{print $5}'
```

4. Now rather extract the month, day and year of creation of the folder bin
```
ls -ld | awk '{print $6, $7, $8}'
```

5. Now rearrange the instruction to get the following output format : 2020-
Oct-26 (from original data : Oct 26 2020)
```
ls -ld | awk '{print $7"-"$6"-"$8}'
```

```

```

```

```
