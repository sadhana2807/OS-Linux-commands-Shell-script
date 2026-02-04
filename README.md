# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

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
<img width="602" height="117" alt="Screenshot from 2026-02-04 13-06-10" src="https://github.com/user-attachments/assets/a69dd155-7346-4d05-88f0-45da178a6ed7" />




cat < file2
## OUTPUT
<img width="604" height="135" alt="Screenshot from 2026-02-04 13-06-25" src="https://github.com/user-attachments/assets/46532578-d4a3-461a-b8f1-bd68ff5282e4" />

# Comparing Files
cmp file1 file2
## OUTPUT
<img width="604" height="52" alt="Screenshot from 2026-02-04 13-06-36" src="https://github.com/user-attachments/assets/abdd11fb-ff03-49da-8593-cea9885d00a5" />

 
comm file1 file2
 ## OUTPUT
 <img width="604" height="184" alt="Screenshot from 2026-02-04 13-06-47" src="https://github.com/user-attachments/assets/495a78a1-2e9b-43b1-9477-986ed8c609d2" />
 
diff file1 file2
## OUTPUT
<img width="604" height="233" alt="Screenshot from 2026-02-04 13-06-59" src="https://github.com/user-attachments/assets/027db459-1e1d-4006-b5fb-19d6cb3aa569" />




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
<img width="424" height="75" alt="Screenshot from 2026-02-04 13-25-19" src="https://github.com/user-attachments/assets/fa7551bc-6e14-4f06-b3c5-8637e9b552d0" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="424" height="94" alt="Screenshot from 2026-02-04 13-25-31" src="https://github.com/user-attachments/assets/ce712f6e-7069-4bbc-9a02-d08dca05b30d" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="424" height="94" alt="Screenshot from 2026-02-04 13-25-40" src="https://github.com/user-attachments/assets/7438da1a-9325-4b25-b934-72b02c7001f9" />

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
<img width="424" height="53" alt="Screenshot from 2026-02-04 13-26-08" src="https://github.com/user-attachments/assets/7b9227f9-957f-4c4c-9fb7-df62c93f48ed" />



grep hello newfile 
## OUTPUT
<img width="424" height="53" alt="Screenshot from 2026-02-04 13-26-15" src="https://github.com/user-attachments/assets/5cca6a68-f16a-4a0f-89a5-a2796dc61693" />




grep -v hello newfile 
## OUTPUT
<img width="424" height="53" alt="Screenshot from 2026-02-04 13-26-22" src="https://github.com/user-attachments/assets/9c38b2ea-65f3-4b33-8cd9-94bca479889e" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="424" height="73" alt="Screenshot from 2026-02-04 13-26-31" src="https://github.com/user-attachments/assets/33fc2e37-d5ed-43ff-a69b-23e8b0ddd3d4" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="464" height="59" alt="Screenshot from 2026-02-04 13-26-51" src="https://github.com/user-attachments/assets/74ea8755-f53e-460d-acc1-43ae9d9eb742" />




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="464" height="70" alt="Screenshot from 2026-02-04 13-27-04" src="https://github.com/user-attachments/assets/053afc6f-44bf-4911-a48e-ae253729aef7" />


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
<img width="487" height="83" alt="Screenshot from 2026-02-04 13-49-55" src="https://github.com/user-attachments/assets/4fe46b59-b725-400a-835c-defc5cc35f7b" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="487" height="83" alt="Screenshot from 2026-02-04 13-50-01" src="https://github.com/user-attachments/assets/c36d5dfa-2774-4264-8dfa-5a9a99c14a03" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="487" height="83" alt="Screenshot from 2026-02-04 13-50-15" src="https://github.com/user-attachments/assets/ed7459b4-9fd7-45f2-9aba-772f8bb8f853" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="487" height="60" alt="Screenshot from 2026-02-04 13-50-26" src="https://github.com/user-attachments/assets/2f581656-f646-4ef2-ae87-8ce075022dd5" />



egrep '(world$)' newfile 
## OUTPUT
<img width="487" height="69" alt="Screenshot from 2026-02-04 13-50-36" src="https://github.com/user-attachments/assets/d5899666-8f2a-4500-a6db-7d572fa3fc9a" />



egrep '(World$)' newfile 
## OUTPUT
<img width="487" height="55" alt="Screenshot from 2026-02-04 13-50-44" src="https://github.com/user-attachments/assets/1ec4235b-f9fb-41cc-9f55-26022e8cc6c3" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="487" height="73" alt="Screenshot from 2026-02-04 13-50-52" src="https://github.com/user-attachments/assets/fd0877c6-8f53-477d-be36-76a1ec19871b" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="487" height="52" alt="Screenshot from 2026-02-04 13-51-13" src="https://github.com/user-attachments/assets/d5c6d9f4-f61d-4d43-b84c-8a72992cb59a" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="487" height="52" alt="Screenshot from 2026-02-04 13-51-19" src="https://github.com/user-attachments/assets/ba3626fe-5467-4d49-8e76-9434a76f5481" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="487" height="52" alt="Screenshot from 2026-02-04 13-51-25" src="https://github.com/user-attachments/assets/7340b625-de8b-4ed7-853d-45c832779e8b" />


egrep l{2} newfile
## OUTPUT
<img width="487" height="72" alt="Screenshot from 2026-02-04 13-51-37" src="https://github.com/user-attachments/assets/4925ed49-d308-4628-9e9e-fdf3db31b330" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="487" height="91" alt="Screenshot from 2026-02-04 13-51-47" src="https://github.com/user-attachments/assets/31d1af28-eeae-4bf5-ba8f-0f0b4899093e" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
<img width="487" height="54" alt="Screenshot from 2026-02-04 14-00-52" src="https://github.com/user-attachments/assets/f5fa13c7-e88e-439e-9bb3-b73dc0023cee" />



sed -n -e '$p' file23
## OUTPUT
<img width="487" height="54" alt="Screenshot from 2026-02-04 14-00-57" src="https://github.com/user-attachments/assets/d2f55970-fe70-47cf-b249-65b9f2a3d6b0" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="487" height="201" alt="Screenshot from 2026-02-04 14-01-05" src="https://github.com/user-attachments/assets/1f2031de-89dd-4905-bc0c-c7da6e16f6ee" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="487" height="201" alt="Screenshot from 2026-02-04 14-01-13" src="https://github.com/user-attachments/assets/be22fb81-bd16-4492-88a1-a36509a9032e" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="487" height="209" alt="Screenshot from 2026-02-04 14-01-24" src="https://github.com/user-attachments/assets/e3e53e6c-72f7-4188-87ca-f418e48822dd" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="487" height="138" alt="Screenshot from 2026-02-04 14-01-42" src="https://github.com/user-attachments/assets/4ae0b54a-fb6d-4ce7-9fde-a87ca902614c" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="487" height="106" alt="Screenshot from 2026-02-04 14-01-53" src="https://github.com/user-attachments/assets/78b293ab-0946-48cc-895a-a6f8358b7672" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="505" height="72" alt="Screenshot from 2026-02-04 14-02-06" src="https://github.com/user-attachments/assets/be933976-930b-4bac-8c99-f4e1778f7303" />



seq 10 
## OUTPUT
<img width="505" height="253" alt="Screenshot from 2026-02-04 14-02-15" src="https://github.com/user-attachments/assets/a84fef86-b160-4962-ba2d-581b9886a95b" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="505" height="95" alt="Screenshot from 2026-02-04 14-09-23" src="https://github.com/user-attachments/assets/b3a17e35-b5ab-452f-9ad2-a045e6d12810" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="505" height="95" alt="Screenshot from 2026-02-04 14-09-29" src="https://github.com/user-attachments/assets/e568f7a7-4c3f-4d1f-8565-3ff391af26c9" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="505" height="121" alt="Screenshot from 2026-02-04 14-09-37" src="https://github.com/user-attachments/assets/a9e7f706-e377-4e18-84b9-113aae929992" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="505" height="106" alt="Screenshot from 2026-02-04 14-09-47" src="https://github.com/user-attachments/assets/480e27aa-2520-47cf-bc54-1c470eb4e41b" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="505" height="106" alt="Screenshot from 2026-02-04 14-09-57" src="https://github.com/user-attachments/assets/b8167e48-7401-4020-92d1-8028da5a41f3" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="505" height="106" alt="Screenshot from 2026-02-04 14-11-44" src="https://github.com/user-attachments/assets/ecb6e5f3-bf3c-438d-9672-b2c48838d0e5" />



sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
<img width="505" height="134" alt="Screenshot from 2026-02-04 14-19-08" src="https://github.com/user-attachments/assets/d6b603b6-8912-4e08-bfa4-c5b11e5938d3" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
<img width="505" height="146" alt="Screenshot from 2026-02-04 14-19-16" src="https://github.com/user-attachments/assets/fe438515-1627-47bd-b22c-160243e0e50e" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="536" height="203" alt="Screenshot from 2026-02-04 14-19-34" src="https://github.com/user-attachments/assets/491abacc-01fb-4518-a599-a789b1dda199" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="536" height="92" alt="Screenshot from 2026-02-04 14-20-01" src="https://github.com/user-attachments/assets/8b6f3635-b403-435a-b2cd-3f73c7b2c171" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="570" height="92" alt="Screenshot from 2026-02-04 14-20-11" src="https://github.com/user-attachments/assets/86cbbf40-772c-4270-8bec-fc8d7de0e623" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1049" height="323" alt="Screenshot from 2026-02-04 14-42-09" src="https://github.com/user-attachments/assets/c689a795-879a-4087-9fb5-812fcef56d01" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


<img width="1049" height="323" alt="Screenshot from 2026-02-04 14-42-20" src="https://github.com/user-attachments/assets/305d622d-ccf7-4460-9d54-2a9d9cb23ee1" />


tar -xvf backup.tar
## OUTPUT

<img width="1049" height="323" alt="Screenshot from 2026-02-04 14-42-29" src="https://github.com/user-attachments/assets/f756368f-ba28-48a8-9aa7-5c4a9b3893da" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="480" height="59" alt="Screenshot from 2026-02-04 14-37-02" src="https://github.com/user-attachments/assets/f6148efa-35dc-4861-bf5e-7326c67122b0" />

gunzip backup.tar.gz
## OUTPUT
<img width="540" height="144" alt="Screenshot from 2026-02-04 14-37-15" src="https://github.com/user-attachments/assets/b2dc2366-927a-46d3-96e6-16129709d86f" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="433" height="80" alt="Screenshot from 2026-02-04 14-49-27" src="https://github.com/user-attachments/assets/909bfb55-86f4-4f5c-9d6d-dda66220192c" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="433" height="100" alt="Screenshot from 2026-02-04 14-49-38" src="https://github.com/user-attachments/assets/78e41e16-0a9e-4380-bd11-72b0e07a4b42" />


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
<img width="587" height="451" alt="image" src="https://github.com/user-attachments/assets/979b3978-e46e-48c7-9822-30d51c39d85b" />

 
ls file1
## OUTPUT
<img width="366" height="65" alt="image" src="https://github.com/user-attachments/assets/85f3638a-541c-4f5a-9b53-76c379d1b72e" />

echo $?
## OUTPUT 
<img width="380" height="66" alt="image" src="https://github.com/user-attachments/assets/158d8dd6-46d3-40d7-9d8a-75baaefed1b9" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="343" height="80" alt="image" src="https://github.com/user-attachments/assets/0669c65f-8941-4c49-b4da-428c50629359" />

abcd
 
echo $?
 ## OUTPUT
<img width="662" height="304" alt="image" src="https://github.com/user-attachments/assets/8db931f3-a475-404f-98a0-400df0343f63" />


 
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
##OUTPUT
<img width="674" height="346" alt="image" src="https://github.com/user-attachments/assets/d856c30a-0f51-45d0-b012-97739a4c92df" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="789" height="324" alt="image" src="https://github.com/user-attachments/assets/6d99a629-765a-4c12-bd6c-b1f9d6056935" />

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
<img width="778" height="238" alt="image" src="https://github.com/user-attachments/assets/ff32ed5a-a40e-4c6a-bbac-36a12b403b14" />

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

<img width="719" height="564" alt="image" src="https://github.com/user-attachments/assets/c06ee760-44ea-4c02-9139-3006c3f836b3" />


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
##OUTPUT
<img width="749" height="654" alt="image" src="https://github.com/user-attachments/assets/8d4b0838-7a9e-4b5f-adde-5836670183b2" />

# check if a file
cat > ifnested.sh 
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
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
<img width="771" height="664" alt="image" src="https://github.com/user-attachments/assets/5bfdecf5-a3a3-4465-839a-2ba59da32912" />

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
<img width="764" height="654" alt="image" src="https://github.com/user-attachments/assets/014ca3c9-bd8e-4333-ad18-4c564310f5d2" />


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="683" height="347" alt="image" src="https://github.com/user-attachments/assets/6ee929cd-a212-4130-9178-2000c73d95dd" />

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
<img width="652" height="220" alt="image" src="https://github.com/user-attachments/assets/ad574257-de12-4db0-af0f-a7498e178e08" />

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
<img width="621" height="307" alt="image" src="https://github.com/user-attachments/assets/a4278090-84c7-444d-9e75-8e815fdedbdc" />


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
<img width="526" height="280" alt="image" src="https://github.com/user-attachments/assets/7d3a2e8a-9fa5-443a-9514-1267c22e149f" />

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
<<img width="779" height="287" alt="image" src="https://github.com/user-attachments/assets/3aecc3e8-c147-4b72-9cbd-e7ad1f7bd976" />


 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
<img width="785" height="295" alt="image" src="https://github.com/user-attachments/assets/fca08ddd-d6b1-4832-be60-b261d77448e8" />

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 <img width="785" height="309" alt="image" src="https://github.com/user-attachments/assets/502cd8b0-e5f9-4e66-9cf2-b0040ff72914" />

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT

<img width="622" height="191" alt="image" src="https://github.com/user-attachments/assets/56415441-2a39-4a6d-a276-377d44be5d4b" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="684" height="146" alt="image" src="https://github.com/user-attachments/assets/b606867f-c5f0-45e2-93bf-63cca35cf3b7" />


$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 <img width="670" height="19" alt="image" src="https://github.com/user-attachments/assets/790e8e97-a7ac-4611-bc83-4c246ecc4d1a" />

 ./funcex.sh 1 2
<img width="648" height="25" alt="image" src="https://github.com/user-attachments/assets/7d562db0-8d36-4be5-b02a-b9812c999c97" />

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
<img width="646" height="54" alt="image" src="https://github.com/user-attachments/assets/89cd0df9-3968-4980-a9da-939b8b9200e0" />

$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
<img width="778" height="68" alt="image" src="https://github.com/user-attachments/assets/2f2cacf9-9e70-4162-89c4-aa261c303c03" />

$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 <img width="716" height="382" alt="image" src="https://github.com/user-attachments/assets/888c38fa-b68d-4e9c-a566-d5f1dce3583c" />

 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 <img width="484" height="252" alt="image" src="https://github.com/user-attachments/assets/6ca56c7a-72d0-4745-aee0-8d0c6bdad1fb" />

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
<img width="609" height="75" alt="image" src="https://github.com/user-attachments/assets/9c991cc1-1aea-4ef5-805a-b2eed172a9f4" />


# RESULT:
The Commands are executed successfully.
