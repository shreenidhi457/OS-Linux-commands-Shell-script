# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting
## NAME:SHREENIDHI S 
## REG NO:212225040410
# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS: 

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT


<img width="523" height="117" alt="Screenshot 2026-10-29 104109" src="https://github.com/user-attachments/assets/1a1837ef-fd7b-4b54-b089-a835fd96e83d" />

cat < file2
## OUTPUT

<img width="503" height="128" alt="Screenshot 2026-10-29 104120" src="https://github.com/user-attachments/assets/94b4dfcd-fa39-4a8a-9bda-d2bbcc9302ce" />

# Comparing Files


cmp file1 file2
## OUTPUT
<img width="551" height="47" alt="Screenshot 2026-10-29 104145" src="https://github.com/user-attachments/assets/529c8b03-25c2-4624-9a36-b77b94907a22" />


comm file1 file2
 ## OUTPUT
  <img width="540" height="272" alt="Screenshot 2026-10-29 104155" src="https://github.com/user-attachments/assets/07b8377d-03fc-448b-b12e-87a401fc5af1" />



diff file1 file2
## OUTPUT

 <img width="587" height="225" alt="Screenshot 2026-10-29 104233" src="https://github.com/user-attachments/assets/6bcf7f66-f69c-45ca-880f-6adccddb7273" />



#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

<img width="593" height="100" alt="Screenshot 2026-10-29 104318" src="https://github.com/user-attachments/assets/3420e30b-ae51-4ce1-bea0-b846a18cf687" />

cut -d "|" -f 1 file22
## OUTPUT


<img width="683" height="113" alt="Screenshot 2026-10-29 104327" src="https://github.com/user-attachments/assets/6e613f81-6b3c-4249-965e-50bf2f00d7ea" />

cut -d "|" -f 2 file22
## OUTPUT

<img width="651" height="112" alt="Screenshot 2026-10-29 104334" src="https://github.com/user-attachments/assets/b7943241-9b41-4304-b80a-01b102abf367" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

<img width="635" height="50" alt="Screenshot 2026-10-29 104422" src="https://github.com/user-attachments/assets/71500054-8afd-4666-ac38-90ca7b7f20f8" />



grep hello newfile 
## OUTPUT


<img width="611" height="45" alt="Screenshot 2026-10-29 104432" src="https://github.com/user-attachments/assets/6bad7d8d-3ef6-488d-bbb3-3bc0e841ce58" />



grep -v hello newfile 
## OUTPUT

<img width="620" height="45" alt="Screenshot 2026-10-29 104556" src="https://github.com/user-attachments/assets/ea57798b-20fb-4557-9e15-a8fb249d7b33" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="732" height="67" alt="Screenshot 2026-10-29 104604" src="https://github.com/user-attachments/assets/d3e5ea3d-638d-4e06-94b4-bf9cdc7a64d6" />





cat newfile | grep -i -c "hello"
## OUTPUT


<img width="645" height="66" alt="Screenshot 2026-10-29 105346" src="https://github.com/user-attachments/assets/851c18c2-f493-46ee-8fc7-b02e54f646e6" />



grep -R ubuntu /etc
## OUTPUT


<img width="738" height="76" alt="Screenshot 2026-10-29 105413" src="https://github.com/user-attachments/assets/4c852c69-f14b-4d36-9c7c-ebd1c3b1b816" />


grep -w -n world newfile   
## OUTPUT
<img width="653" height="62" alt="Screenshot 2026-10-29 105836" src="https://github.com/user-attachments/assets/15c8e0f4-fe71-4fa0-9532-89049507f595" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="702" height="60" alt="Screenshot 2026-10-29 105848" src="https://github.com/user-attachments/assets/41687b59-10f5-41b8-b5a9-32ce567130c4" />



egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="595" height="35" alt="Screenshot 2026-10-29 105854" src="https://github.com/user-attachments/assets/3326fca7-76a9-48dc-8ae8-80f43dd0793e" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="635" height="63" alt="Screenshot 2026-10-29 105857" src="https://github.com/user-attachments/assets/6951ff50-8914-4357-a7f6-5a52dd31a864" />






egrep '(^hello)' newfile 
## OUTPUT

<img width="730" height="102" alt="Screenshot 2026-10-30 095056" src="https://github.com/user-attachments/assets/50d1cd98-5edf-4ee3-8417-ec7186e19936" />



egrep '(world$)' newfile 
## OUTPUT

<img width="632" height="46" alt="Screenshot 2026-10-30 095144" src="https://github.com/user-attachments/assets/5ce1c4ea-4360-4ba7-95fe-5112d7687697" />


egrep '(World$)' newfile 
## OUTPUT


<img width="716" height="45" alt="Screenshot 2026-10-30 095203" src="https://github.com/user-attachments/assets/65a8b763-7431-41f1-9df0-be26716efa2d" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="503" height="45" alt="Screenshot 2026-10-30 095230" src="https://github.com/user-attachments/assets/3704e1d4-6f53-4606-8c9b-a00b9e9c8a36" />




egrep '[1-9]' newfile 
## OUTPUT



<img width="575" height="70" alt="Screenshot 2026-10-30 095254" src="https://github.com/user-attachments/assets/79060978-f772-411b-a0e5-319b605cd809" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="725" height="90" alt="Screenshot 2026-10-30 095412" src="https://github.com/user-attachments/assets/5338dda7-3c6b-4593-b4f9-fa3bad1b76d4" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="626" height="51" alt="Screenshot 2026-10-30 095702" src="https://github.com/user-attachments/assets/5e697802-c600-4462-84c7-23a6e00c54fe" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="610" height="47" alt="Screenshot 2026-10-30 104832" src="https://github.com/user-attachments/assets/931af32c-2150-45ab-8163-1daa087a0b5a" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="563" height="85" alt="Screenshot 2026-10-30 104905" src="https://github.com/user-attachments/assets/c212feaf-f53b-46c3-992a-ba9daae2f90c" />

cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="836" height="318" alt="Screenshot 2026-10-30 105201" src="https://github.com/user-attachments/assets/7eec3233-e17d-41b9-b991-f62eedbcce65" />


 
ls file1
## OUTPUT

<img width="475" height="50" alt="Screenshot 2026-10-30 105214" src="https://github.com/user-attachments/assets/0c93a416-4e30-4a32-b385-409fe1a20eeb" />

echo $?
## OUTPUT 

<img width="458" height="47" alt="Screenshot 2026-10-30 105227" src="https://github.com/user-attachments/assets/dc18a3bb-7b29-453a-b24f-276309499974" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="776" height="112" alt="Screenshot 2026-10-30 105301" src="https://github.com/user-attachments/assets/75fa258e-29ed-47fe-a039-a3ffca505bfd" />

abcd
 
echo $?
 ## OUTPUT
<img width="497" height="92" alt="Screenshot 2026-10-30 105343" src="https://github.com/user-attachments/assets/c012b888-1b89-4d74-8d3e-5adbfb76755a" />



 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```





chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


<img width="777" height="65" alt="Screenshot 2026-10-30 110026" src="https://github.com/user-attachments/assets/5ad8b09e-90ff-4845-9901-6b8708fd4e79" />

# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
<img width="675" height="40" alt="Screenshot 2026-10-30 110533" src="https://github.com/user-attachments/assets/ef599271-0190-490b-b0f9-d1afb5f3bb04" />




# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
<img width="685" height="96" alt="Screenshot 2026-10-31 084413" src="https://github.com/user-attachments/assets/acc04753-7d70-44ff-b315-ca240f740002" />



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 

## OUTPUT

<img width="533" height="62" alt="Screenshot 2026-10-31 083957" src="https://github.com/user-attachments/assets/378dbb60-507d-439a-9b68-32785697953b" />


# RESULT:
The Commands are executed successfully.
