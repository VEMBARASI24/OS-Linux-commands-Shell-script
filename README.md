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
<img width="612" height="287" alt="image" src="https://github.com/user-attachments/assets/87a1e9f1-661c-4bb2-8e92-a3c71480b2b5" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="417" height="123" alt="image" src="https://github.com/user-attachments/assets/6243d0e5-abd7-4a79-adb5-949ad0314e74" />



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
<img width="602" height="337" alt="image" src="https://github.com/user-attachments/assets/017a6efe-19d9-4ff7-9ae7-9dd0caea74f6" />


 
ls file1
## OUTPUT
<img width="445" height="52" alt="image" src="https://github.com/user-attachments/assets/e1d1bb45-71c9-4f81-a34d-c1baab9b9b55" />


echo $?
## OUTPUT 
<img width="442" height="53" alt="image" src="https://github.com/user-attachments/assets/63b2502d-5f43-42de-a634-0854c2e0f3a3" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="482" height="101" alt="image" src="https://github.com/user-attachments/assets/af8461b1-4cba-4061-989c-cb759ac761e3" />

 
abcd
 
echo $?
 ## OUTPUT
<img width="463" height="105" alt="image" src="https://github.com/user-attachments/assets/981dd0a9-fb8a-4123-b6e1-2e8c2ef034e4" />



 
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
<img width="422" height="217" alt="image" src="https://github.com/user-attachments/assets/70aa0f44-edb0-4d8b-a627-dc83b4e9e386" />




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="618" height="128" alt="image" src="https://github.com/user-attachments/assets/950a7fb4-a552-44e3-80c9-d8cb98e3814d" />



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
<img width="458" height="52" alt="image" src="https://github.com/user-attachments/assets/34e5de9f-7ac1-4417-b8f4-3ca92ae37e7a" />


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
<img width="555" height="61" alt="image" src="https://github.com/user-attachments/assets/aa044465-6503-4110-ad4c-eb7f8fea66a1" />




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
<img width="652" height="112" alt="image" src="https://github.com/user-attachments/assets/04dd7174-4c2b-4e20-ba2a-26c5d8236c07" />


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
<img width="587" height="161" alt="image" src="https://github.com/user-attachments/assets/1b30dee9-0fb6-4e80-930e-a16d661955bf" />

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
<img width="642" height="72" alt="image" src="https://github.com/user-attachments/assets/e22f8819-7742-4cf2-8da3-b5f0f7c4a784" />



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
<img width="615" height="67" alt="image" src="https://github.com/user-attachments/assets/337bd199-280a-46d1-8d37-8aed7621a569" />


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
 <img width="412" height="52" alt="image" src="https://github.com/user-attachments/assets/1e547c6d-6b38-4567-a5fd-76f2cff25f5a" />

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
 <img width="430" height="211" alt="image" src="https://github.com/user-attachments/assets/d597e828-60ed-4d0a-bb66-d599f628a6cf" />


 
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
<img width="795" height="181" alt="image" src="https://github.com/user-attachments/assets/a4428eae-259b-4b5e-8aa8-f46cef6d00cb" />



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
<img width="437" height="132" alt="image" src="https://github.com/user-attachments/assets/77a5dbb6-3023-4d02-966d-d3818d5b6e6c" />


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
<img width="492" height="50" alt="image" src="https://github.com/user-attachments/assets/9ba01231-b7c6-4c40-97e2-c38d5f02f9b4" />


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
<img width="512" height="247" alt="image" src="https://github.com/user-attachments/assets/8543d9d6-84e7-47b7-94c0-3bc0ede3342d" />


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
<img width="670" height="92" alt="image" src="https://github.com/user-attachments/assets/c5bafa38-bc9a-4d2f-83c8-d1becbe32fc3" />


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
<img width="737" height="131" alt="image" src="https://github.com/user-attachments/assets/0e68298c-a0f1-4d82-ba85-298dad244f29" />

 
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
<img width="587" height="72" alt="image" src="https://github.com/user-attachments/assets/450bad86-1422-4796-a9d1-fa83b72c0710" />



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
<img width="648" height="72" alt="image" src="https://github.com/user-attachments/assets/6eee08bf-cc18-41ee-9ef2-943bde494f82" />


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
<img width="477" height="267" alt="image" src="https://github.com/user-attachments/assets/0dc53085-6708-418b-ad33-e771b80de529" />


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
<img width="571" height="422" alt="image" src="https://github.com/user-attachments/assets/ce9d71f6-5594-4134-9702-51985ec866d9" />



# RESULT:
The Commands are executed successfully.
