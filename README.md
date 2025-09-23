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
<img width="752" height="180" alt="image" src="https://github.com/user-attachments/assets/9da3cbd0-7d82-4924-9873-5963335dd8be" />



cat < file2
## OUTPUT
<img width="762" height="219" alt="image" src="https://github.com/user-attachments/assets/1b898f23-480f-4572-af54-02d51398440e" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="955" height="113" alt="image" src="https://github.com/user-attachments/assets/0f3b5e53-3125-4c4e-90ed-b325d37a3c43" />

comm file1 file2
 ## OUTPUT

 
diff file1 file2
## OUTPUT
<img width="760" height="333" alt="image" src="https://github.com/user-attachments/assets/3bb0fdc2-373a-4302-8070-bdb8120564ca" />


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
<img width="755" height="118" alt="image" src="https://github.com/user-attachments/assets/ad343992-847e-4536-983d-b83bb3fb8c16" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="807" height="147" alt="image" src="https://github.com/user-attachments/assets/b5312e67-be05-40a1-908f-2dd81f41bd57" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="773" height="156" alt="image" src="https://github.com/user-attachments/assets/5d5e702f-c025-4884-9daa-64f08ff205cc" />


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
<img width="743" height="85" alt="image" src="https://github.com/user-attachments/assets/e62146c3-798a-43bc-ae89-ed5cee2e1ea0" />



grep hello newfile 
## OUTPUT

<img width="751" height="91" alt="image" src="https://github.com/user-attachments/assets/11bb9207-67ac-4dde-b57d-c56f39cf4202" />



grep -v hello newfile 
## OUTPUT
<img width="748" height="94" alt="image" src="https://github.com/user-attachments/assets/aefb0cb9-0adc-44d1-b937-f666e8ff20a9" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="755" height="123" alt="image" src="https://github.com/user-attachments/assets/24edb450-8d8b-46c3-8b98-67cfafec85b3" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="754" height="86" alt="image" src="https://github.com/user-attachments/assets/6da73101-57c4-4b34-bfe9-394224d1fe69" />



grep -R ubuntu /etc
## OUTPUT
<img width="1261" height="342" alt="image" src="https://github.com/user-attachments/assets/fc377a33-9a60-4a44-a9a4-d37d5dee3927" />



grep -w -n world newfile   
## OUTPUT
<img width="745" height="125" alt="image" src="https://github.com/user-attachments/assets/247e19a6-b9b4-4f48-aa2e-b1b106e0247b" />


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
<img width="747" height="124" alt="image" src="https://github.com/user-attachments/assets/1b5913a5-ca29-4dd6-b8ed-c6d6e1b65b46" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="762" height="124" alt="image" src="https://github.com/user-attachments/assets/5b5880e0-dd93-4e48-a85c-5f3f566851e7" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="751" height="123" alt="image" src="https://github.com/user-attachments/assets/97d49ff4-40f6-4b50-b856-cb6286a1d976" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="748" height="91" alt="image" src="https://github.com/user-attachments/assets/fd747b17-78fc-49b7-b288-e8ed17bda6ee" />


egrep '(world$)' newfile 
## OUTPUT
<img width="752" height="111" alt="image" src="https://github.com/user-attachments/assets/a182ab7e-d173-4cc3-bde4-6b9884487f0f" />



egrep '(World$)' newfile 
## OUTPUT
<img width="743" height="87" alt="image" src="https://github.com/user-attachments/assets/fedfbed0-a095-45e1-aceb-4d60b73fc10a" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="742" height="187" alt="image" src="https://github.com/user-attachments/assets/4aed8d56-9eec-4ad1-84ff-a85ca27da3c2" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="747" height="90" alt="image" src="https://github.com/user-attachments/assets/271d3f1b-8293-4060-a09f-9a8b09b5a160" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="751" height="87" alt="image" src="https://github.com/user-attachments/assets/a74a2399-47d8-4084-9292-839ffd7a8098" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="756" height="86" alt="image" src="https://github.com/user-attachments/assets/50e179c9-9324-4372-b79b-716f9b5947b6" />


egrep l{2} newfile
## OUTPUT
<img width="751" height="118" alt="image" src="https://github.com/user-attachments/assets/d4ba1ffe-b4b6-4a4b-b3a4-3b6aa76e2e22" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="784" height="144" alt="image" src="https://github.com/user-attachments/assets/89671e31-dbec-418f-bd15-bfc52e1308e3" />


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
<img width="1111" height="120" alt="image" src="https://github.com/user-attachments/assets/e9369d43-cc1d-4b0f-99e0-41eae5c42d13" />



sed -n -e '$p' file23
## OUTPUT
<img width="1108" height="122" alt="image" src="https://github.com/user-attachments/assets/22dcd480-5589-4593-87d5-dbe345874fac" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1119" height="426" alt="image" src="https://github.com/user-attachments/assets/ea2d4f5b-8dd3-423f-aa4c-a8e3da825a4b" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="1181" height="426" alt="image" src="https://github.com/user-attachments/assets/95907086-f98c-4f9a-87ee-9f87665f83c1" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="1121" height="420" alt="image" src="https://github.com/user-attachments/assets/85ee7f57-5406-46c7-9c25-a9c55f675e66" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="1121" height="290" alt="image" src="https://github.com/user-attachments/assets/8acfe266-f26f-46da-a0bc-40aafc7a742e" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="1144" height="213" alt="image" src="https://github.com/user-attachments/assets/0862d0f9-849d-4c95-9fa8-3cf041d3a698" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1118" height="173" alt="image" src="https://github.com/user-attachments/assets/ddabbd9e-44f4-4188-976d-408d1bd11a9e" />


seq 10 
## OUTPUT
<img width="1121" height="517" alt="image" src="https://github.com/user-attachments/assets/c7ea9942-abb7-429a-96d1-fdf66987b980" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1107" height="212" alt="image" src="https://github.com/user-attachments/assets/3697956a-1020-4287-951d-2017cf3637a0" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="1132" height="242" alt="image" src="https://github.com/user-attachments/assets/18196f37-7a76-4871-9e4c-06243903dbca" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="1133" height="232" alt="image" src="https://github.com/user-attachments/assets/94a3d23f-1cb6-44a0-a6da-b8ff556e7fb9" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="1178" height="203" alt="image" src="https://github.com/user-attachments/assets/c32f77ab-50b1-49cf-98b8-d9857b8d4dc9" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1176" height="206" alt="image" src="https://github.com/user-attachments/assets/aff1b4ad-9a31-457c-aca4-91c8c00c0ead" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="1125" height="206" alt="image" src="https://github.com/user-attachments/assets/24314769-416c-48e6-899a-51069e640777" />



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
<img width="1124" height="294" alt="image" src="https://github.com/user-attachments/assets/4b4899f7-fab2-4aba-9778-f5810c5a99a4" />


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
<img width="1118" height="300" alt="image" src="https://github.com/user-attachments/assets/61cd7b20-1a06-4eb1-ba4c-0d6b8760c7a5" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1152" height="431" alt="image" src="https://github.com/user-attachments/assets/5a5e7e9b-6beb-4a4e-86e5-09230cc282d1" />

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
<img width="1128" height="212" alt="image" src="https://github.com/user-attachments/assets/155eb493-27f7-4169-ab25-566a3222e87a" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1126" height="208" alt="image" src="https://github.com/user-attachments/assets/d964f6fd-777a-44c2-9e21-de01d3b91891" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1155" height="824" alt="image" src="https://github.com/user-attachments/assets/5be4b00f-d60b-4eac-a14e-07cd9da1bc36" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1242" height="729" alt="image" src="https://github.com/user-attachments/assets/bae5f3d4-6bde-432e-9ba4-cfd2ce6c100b" />


tar -xvf backup.tar
## OUTPUT
<img width="1236" height="799" alt="image" src="https://github.com/user-attachments/assets/127ba3c0-6f46-4c33-a31c-74485e80cdcb" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1252" height="116" alt="image" src="https://github.com/user-attachments/assets/0054b3ba-b16f-4cd2-b578-8199d531fcf0" />

gunzip backup.tar.gz
## OUTPUT
<img width="1252" height="75" alt="image" src="https://github.com/user-attachments/assets/b9f1a3cb-dfc1-4d9e-a16e-9f60ac82936e" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="975" height="180" alt="image" src="https://github.com/user-attachments/assets/feb32b30-0093-4ee4-b9a6-c287aac6f7bd" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="992" height="174" alt="image" src="https://github.com/user-attachments/assets/a9934e16-0e2b-472c-9899-8d3036e43f94" />


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
<img width="1119" height="669" alt="image" src="https://github.com/user-attachments/assets/58738ed1-bd78-4de5-b0f4-4bd1583de6ac" />

 
ls file1
## OUTPUT
<img width="982" height="96" alt="image" src="https://github.com/user-attachments/assets/0c111e4b-df42-4c18-92b8-219d17390b64" />

echo $?
## OUTPUT 
<img width="959" height="104" alt="image" src="https://github.com/user-attachments/assets/bba297e0-367f-4965-85d7-c5b9ada1257e" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="1049" height="209" alt="image" src="https://github.com/user-attachments/assets/fe4c7356-5ff9-4d81-9a00-fb1182f61bdb" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="1040" height="212" alt="image" src="https://github.com/user-attachments/assets/9700f83c-71a9-4b79-b93e-45b0ba1b6899" />


 
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
<img width="996" height="403" alt="image" src="https://github.com/user-attachments/assets/f6fb4a91-7646-40ae-8d39-982eab51788c" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="975" height="141" alt="image" src="https://github.com/user-attachments/assets/6d9b5c4c-a80c-4c80-8929-d833e47a6b11" />


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
<img width="968" height="106" alt="image" src="https://github.com/user-attachments/assets/32095ad4-41fa-4574-b557-75232f365e8f" />

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
<img width="977" height="106" alt="image" src="https://github.com/user-attachments/assets/7afeedfe-8f02-4553-b397-c48d557d4132" />



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
<img width="1083" height="178" alt="image" src="https://github.com/user-attachments/assets/f6d81d1c-53ba-42c6-8afd-d65ca81aa8e1" />

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
## OUTPUT
<img width="1034" height="222" alt="image" src="https://github.com/user-attachments/assets/069990ea-4954-498a-b342-7b88c2555f81" />

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
<img width="1042" height="139" alt="image" src="https://github.com/user-attachments/assets/93dc3d38-c0f6-470e-9d01-5c83f346d64e" />


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
<img width="1032" height="145" alt="image" src="https://github.com/user-attachments/assets/419e57e5-b63d-4d33-a13b-b7a83b357332" />

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
## OUTPUT
 <img width="992" height="113" alt="image" src="https://github.com/user-attachments/assets/de6f5b65-36ee-417e-ac7f-f1a893f2bcfb" />

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
## OUTPUT
 <img width="1024" height="440" alt="image" src="https://github.com/user-attachments/assets/4ee3bfd8-c000-4ac6-8ddc-69c45a9ff34a" />

 
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
<img width="1257" height="363" alt="image" src="https://github.com/user-attachments/assets/67a29537-4053-4f64-8196-2a64e32d128c" />


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
<img width="991" height="253" alt="image" src="https://github.com/user-attachments/assets/fefd254a-7476-4eba-8a92-7329fc8cd74f" />

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
<img width="967" height="114" alt="image" src="https://github.com/user-attachments/assets/81f61473-e9aa-421c-9b23-3a04ab9fe59d" />

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

 <img width="985" height="518" alt="image" src="https://github.com/user-attachments/assets/734aac54-fe40-48e4-8bf0-052b53dfcd77" />

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
<img width="1133" height="183" alt="image" src="https://github.com/user-attachments/assets/73e2e864-d837-48d2-9d12-f7da5debd125" />

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
<img width="1195" height="249" alt="image" src="https://github.com/user-attachments/assets/a3bd81bd-6460-4ea6-824c-3313248266e5" />
 
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
<img width="990" height="149" alt="image" src="https://github.com/user-attachments/assets/a973ddde-ef9c-4a17-a60c-42e735e84975" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh
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
<img width="1114" height="150" alt="image" src="https://github.com/user-attachments/assets/da3a4b08-4cea-425c-a466-eac40bceb2c9" />

 ./funcex.sh 

 
 ./funcex.sh 1 2

 
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
<img width="1029" height="219" alt="image" src="https://github.com/user-attachments/assets/78a532e9-869e-4149-8eec-4e9dfb82f17e" />

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
$ ./argshift.sh 1 2 3
 <img width="900" height="159" alt="image" src="https://github.com/user-attachments/assets/d6006dd0-2f53-4bf7-9cc6-28b2d0beb0c6" />

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
 <img width="927" height="523" alt="image" src="https://github.com/user-attachments/assets/7247187d-9495-4aac-b269-bd354802c931" />

 
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
 <img width="880" height="500" alt="image" src="https://github.com/user-attachments/assets/feaeb94a-bea0-440b-aacc-121efea3230d" />

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
<img width="1132" height="778" alt="image" src="https://github.com/user-attachments/assets/e782553d-9632-47df-892b-8284a334f27b" />


# RESULT:
The Commands are executed successfully.
