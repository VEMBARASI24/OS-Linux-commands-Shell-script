# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting
# NAME: VEMBARASI.A.R
## REG NO: 212224220120
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
<img width="365" height="110" alt="image" src="https://github.com/user-attachments/assets/bd2143fe-49d9-4977-934c-44569c74d5cb" />




cat < file2
## OUTPUT
<img width="428" height="132" alt="image" src="https://github.com/user-attachments/assets/b563e694-defe-4a9c-942f-a84fc784501b" />



# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="955" height="113" alt="image" src="https://github.com/user-attachments/assets/0f3b5e53-3125-4c4e-90ed-b325d37a3c43" />

comm file1 file2
 ## OUTPUT
<img width="547" height="60" alt="image" src="https://github.com/user-attachments/assets/b89689d2-74db-46df-b400-10eae34eb346" />

 
diff file1 file2
## OUTPUT
<img width="565" height="201" alt="image" src="https://github.com/user-attachments/assets/dc2f0ca7-6ef6-4867-a4ca-1d0e28d8cac0" />


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
<img width="355" height="92" alt="image" src="https://github.com/user-attachments/assets/c548b6eb-35bf-496a-8579-f0cef63a3a0b" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="370" height="111" alt="image" src="https://github.com/user-attachments/assets/b7fa294c-088b-4b19-9903-80f58afebcc5" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="462" height="107" alt="image" src="https://github.com/user-attachments/assets/87bc61a1-f0d0-44da-b388-1c3ba310ab2d" />

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
<img width="333" height="57" alt="image" src="https://github.com/user-attachments/assets/bac9d5da-ecef-4467-a833-325b4883d09c" />




grep hello newfile 
## OUTPUT

<img width="405" height="55" alt="image" src="https://github.com/user-attachments/assets/2b6f06d0-33f1-4284-932e-9872e25dc989" />




grep -v hello newfile 
## OUTPUT
<img width="428" height="53" alt="image" src="https://github.com/user-attachments/assets/278e4510-0b35-4bab-9e3a-649169b8e904" />




cat newfile | grep -i "hello"
## OUTPUT

<img width="472" height="87" alt="image" src="https://github.com/user-attachments/assets/073f02f1-52ac-4416-8548-741db1f47bbf" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="488" height="56" alt="image" src="https://github.com/user-attachments/assets/375f9ef9-20b5-48a8-a487-f52b409b9106" />




grep -R ubuntu /etc
## OUTPUT
<img width="1201" height="272" alt="image" src="https://github.com/user-attachments/assets/dc8bee72-6294-405f-a876-5ef9abe204f4" />


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
<img width="435" height="77" alt="image" src="https://github.com/user-attachments/assets/9071529f-ab7d-44dd-beec-8475df706f08" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="497" height="76" alt="image" src="https://github.com/user-attachments/assets/f52d6c20-203f-444e-b8d0-dfd7ebc77f32" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="487" height="75" alt="image" src="https://github.com/user-attachments/assets/0d707cbb-dc5b-4637-b776-9a82e18865f3" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="453" height="62" alt="image" src="https://github.com/user-attachments/assets/a1096234-f89c-4a50-9fe1-3fe94f8bbc0a" />


egrep '(world$)' newfile 
## OUTPUT
<img width="440" height="76" alt="image" src="https://github.com/user-attachments/assets/dd06e2fd-e6da-46b0-bb72-431105d252b7" />




egrep '(World$)' newfile 
## OUTPUT
<img width="452" height="52" alt="image" src="https://github.com/user-attachments/assets/9927eaa6-12de-4a29-90d0-7b5ae1549f7f" />



egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="450" height="68" alt="image" src="https://github.com/user-attachments/assets/61e49980-b8d4-4fb3-b31d-3a07d3efb6fc" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="460" height="57" alt="image" src="https://github.com/user-attachments/assets/c7775d3a-7881-46f8-b102-902be9a50293" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="482" height="53" alt="image" src="https://github.com/user-attachments/assets/eec72c1c-8a9c-4af6-83fc-0ca1de48ef19" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="411" height="57" alt="image" src="https://github.com/user-attachments/assets/eb6d5528-d2de-44f7-8e58-d02c43272f5d" />


egrep l{2} newfile
## OUTPUT
<img width="436" height="77" alt="image" src="https://github.com/user-attachments/assets/e6828129-21c7-47aa-ba1a-74e4e0ec6db4" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="467" height="91" alt="image" src="https://github.com/user-attachments/assets/9dfb52b6-2b1a-4294-81a5-f4e8b4f3e8ef" />



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
<img width="343" height="57" alt="image" src="https://github.com/user-attachments/assets/1b4d6e53-89a4-43ab-98d0-489ead2040d7" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="472" height="182" alt="image" src="https://github.com/user-attachments/assets/9eea00c0-5175-46a1-9486-b489f9fa7380" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="481" height="183" alt="image" src="https://github.com/user-attachments/assets/fd5bffeb-b782-4090-bed5-be7811183290" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="472" height="185" alt="image" src="https://github.com/user-attachments/assets/5876edae-508e-4e96-afd3-6030f8eef955" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="538" height="127" alt="image" src="https://github.com/user-attachments/assets/69ce3791-d333-4c03-9936-24052de14d45" />




sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="522" height="100" alt="image" src="https://github.com/user-attachments/assets/50411db3-ceed-43af-bf15-f43c556294ac" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="557" height="71" alt="image" src="https://github.com/user-attachments/assets/684ac932-cb27-4e20-bd56-20122ae81527" />



seq 10 
## OUTPUT
<img width="552" height="217" alt="image" src="https://github.com/user-attachments/assets/01d6b812-2ac4-4724-9331-f391f84539a7" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="461" height="90" alt="image" src="https://github.com/user-attachments/assets/3a49a22f-6d33-4ff5-b521-7aa9fc85d520" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="517" height="87" alt="image" src="https://github.com/user-attachments/assets/83fef1ad-29cb-4ea6-b06e-e55dea2fbb90" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="468" height="111" alt="image" src="https://github.com/user-attachments/assets/692ee3d4-cfdc-4c33-9340-d21b4e94d4e2" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="542" height="93" alt="image" src="https://github.com/user-attachments/assets/4336a5fd-4b9c-4be0-8377-d910b567baba" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="520" height="82" alt="image" src="https://github.com/user-attachments/assets/c58c7edd-d46d-4929-8cec-5c644c578a0e" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="561" height="96" alt="image" src="https://github.com/user-attachments/assets/9df1cc45-2e93-46b6-90d6-26d19829ac28" />




sed -n '2,4{s/$/*/;p}' file23
<img width="520" height="96" alt="image" src="https://github.com/user-attachments/assets/b4db7a18-c655-43e6-8155-90ee43741b82" />


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
<img width="447" height="122" alt="image" src="https://github.com/user-attachments/assets/7e3bc382-e958-43b1-8e95-b0c34629a24c" />



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
<img width="463" height="136" alt="image" src="https://github.com/user-attachments/assets/20ce3940-28d9-42da-b519-ef15b5318854" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="647" height="197" alt="image" src="https://github.com/user-attachments/assets/a2d806bf-77c2-49d4-91ec-74fd9843d44a" />


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
<img width="372" height="93" alt="image" src="https://github.com/user-attachments/assets/5c7c5847-b24d-46d8-a2f0-2324fbe4851f" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="542" height="91" alt="image" src="https://github.com/user-attachments/assets/543735a8-31e2-47c6-9a58-75a84ab90db3" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="355" height="322" alt="image" src="https://github.com/user-attachments/assets/4c85adcc-5bf5-46ad-a630-f7ddaa117d0c" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="637" height="332" alt="image" src="https://github.com/user-attachments/assets/f979fa4c-0d1a-49d8-8a7a-43ec618da8b1" />



tar -xvf backup.tar
## OUTPUT
<img width="490" height="327" alt="image" src="https://github.com/user-attachments/assets/96f9ea5a-451a-4fbd-8ad9-4686eec599f1" />


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
