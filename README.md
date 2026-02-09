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
<img width="380" height="115" alt="image" src="https://github.com/user-attachments/assets/4c8c9e26-50f6-4bb1-ae5e-c195d15c6d10" />



cat < file2
## OUTPUT
<img width="380" height="115" alt="image" src="https://github.com/user-attachments/assets/d859bed8-5d9b-4887-ba83-c456d697187c" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="380" height="115" alt="image" src="https://github.com/user-attachments/assets/c481c522-3aa7-4a60-85df-31093b767899" />

comm file1 file2
 ## OUTPUT
<img width="406" height="232" alt="image" src="https://github.com/user-attachments/assets/6d25b4b8-9231-4f19-bcd3-7e25060a45ec" />

 
diff file1 file2
## OUTPUT
<img width="408" height="160" alt="image" src="https://github.com/user-attachments/assets/5a073974-92af-475f-9917-5052097c1cf7" />


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
<img width="414" height="61" alt="image" src="https://github.com/user-attachments/assets/83ae30b7-8cd1-4a0d-8936-5327eabc6c9d" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="415" height="79" alt="image" src="https://github.com/user-attachments/assets/79ea0d15-8863-4201-b135-e83aaae0f7ea" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="425" height="79" alt="image" src="https://github.com/user-attachments/assets/4600970d-3da7-43ed-846e-7987ad0564e9" />

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

<img width="462" height="37" alt="image" src="https://github.com/user-attachments/assets/35f869d6-894c-437f-9344-a0d45514493e" />


grep hello newfile 
## OUTPUT

<img width="462" height="37" alt="image" src="https://github.com/user-attachments/assets/7c4439af-66e2-446b-b052-dd4ae92231ef" />



grep -v hello newfile 
## OUTPUT
<img width="462" height="37" alt="image" src="https://github.com/user-attachments/assets/9f5a82b7-15db-40a8-a510-268c210a3004" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="487" height="56" alt="image" src="https://github.com/user-attachments/assets/b9eabfda-a4eb-4aaf-bc16-7215ee3bd39d" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="489" height="41" alt="image" src="https://github.com/user-attachments/assets/776ad6e9-f47b-43d7-89c0-ee53f385dcf2" />



grep -R ubuntu /etc
## OUTPUT

<img width="1126" height="772" alt="image" src="https://github.com/user-attachments/assets/3736b3d5-ecc7-44e6-8633-e43fe6b519d6" />


grep -w -n world newfile   
## OUTPUT
<img width="534" height="66" alt="image" src="https://github.com/user-attachments/assets/e5376c01-5e9d-49cc-822d-cfb365c5091e" />


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

<img width="534" height="66" alt="image" src="https://github.com/user-attachments/assets/a99f7040-67d7-4c90-9d4e-6760a936cffc" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="545" height="52" alt="image" src="https://github.com/user-attachments/assets/2342b2e4-3a06-42a5-86b8-fd0879579d77" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="545" height="52" alt="image" src="https://github.com/user-attachments/assets/5696b388-2a17-4422-99a6-ba6cfa2cb604" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="547" height="41" alt="image" src="https://github.com/user-attachments/assets/50e923ea-00bf-43ef-9e60-91642394e3b2" />


egrep '(world$)' newfile 
## OUTPUT

<img width="558" height="55" alt="image" src="https://github.com/user-attachments/assets/a95cce4c-2659-4900-b53b-479fe0cd6936" />


egrep '(World$)' newfile 
## OUTPUT
<img width="561" height="39" alt="image" src="https://github.com/user-attachments/assets/bfd78ffa-97ef-4515-bfb4-f417233a66df" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="577" height="72" alt="image" src="https://github.com/user-attachments/assets/c0f6f79a-53f1-4ffe-bbe8-bfb4b09f0dce" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="587" height="40" alt="image" src="https://github.com/user-attachments/assets/140fe6ee-3508-4e80-81dc-94b4ec64d69e" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="587" height="40" alt="image" src="https://github.com/user-attachments/assets/c6431297-7c90-48b3-a502-c0bb249e1e38" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="587" height="40" alt="image" src="https://github.com/user-attachments/assets/bb7975dc-a0ba-44f1-90ca-6ac1773fc82a" />


egrep l{2} newfile
## OUTPUT
<img width="597" height="55" alt="image" src="https://github.com/user-attachments/assets/6e1ca8ee-a4ef-40b6-9260-fbecedb35e28" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="605" height="70" alt="image" src="https://github.com/user-attachments/assets/c604232d-5cde-4135-9b01-aa2fe2a6eb2b" />


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

<img width="574" height="46" alt="image" src="https://github.com/user-attachments/assets/bd4784a0-a450-4782-a32d-756affd1eb5f" />


sed -n -e '$p' file23
## OUTPUT
<img width="559" height="262" alt="image" src="https://github.com/user-attachments/assets/cc714ee1-11c2-4719-989b-909456319503" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="620" height="169" alt="image" src="https://github.com/user-attachments/assets/9c7534f6-e839-4516-b59c-2daf329307e3" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="630" height="180" alt="image" src="https://github.com/user-attachments/assets/176aa54d-a3ec-4d64-b503-0f6b7b7cc259" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT



sed -n -e '1,5p' file23
## OUTPUT

<img width="644" height="200" alt="image" src="https://github.com/user-attachments/assets/abf3f650-011c-4e48-8840-636d7815e6a3" />


sed -n -e '2,/Joe/p' file23
## OUTPUT




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="649" height="77" alt="image" src="https://github.com/user-attachments/assets/e4d2aae1-fa6a-4fd0-8513-7ce0f087ff1a" />



seq 10 
## OUTPUT

<img width="649" height="77" alt="image" src="https://github.com/user-attachments/assets/cce5bcee-106d-4b84-bd86-e8fbfaf90581" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="659" height="95" alt="image" src="https://github.com/user-attachments/assets/27142269-465e-4caf-bb0d-5d045cc48607" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="659" height="95" alt="image" src="https://github.com/user-attachments/assets/c388cf97-c156-46aa-be35-eb88db338030" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="659" height="78" alt="image" src="https://github.com/user-attachments/assets/80fa37a4-3f74-4bcb-a9a6-99a148e42c2c" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="659" height="78" alt="image" src="https://github.com/user-attachments/assets/8880413a-204a-4313-b84e-b1ddab5198f9" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="659" height="78" alt="image" src="https://github.com/user-attachments/assets/8b02ad83-c4d8-4289-87a8-f368e4848080" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="659" height="78" alt="image" src="https://github.com/user-attachments/assets/26f16a9d-fe6d-41d0-93da-441bb717dd88" />



sed -n '2,4{s/$/*/;p}' file23
## output
<img width="629" height="117" alt="image" src="https://github.com/user-attachments/assets/2b9fb60f-54dd-4690-ac44-a6becdfb2260" />



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

<img width="631" height="113" alt="image" src="https://github.com/user-attachments/assets/2ae0fe04-25d8-4c75-a3b0-f8bbf3fcf085" />

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
<img width="697" height="167" alt="image" src="https://github.com/user-attachments/assets/932a7ade-5338-483a-ba93-cc6cba0eb7e0" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="723" height="76" alt="image" src="https://github.com/user-attachments/assets/cd457b23-264c-4ecf-b719-b50388b9fae9" />

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
<img width="723" height="76" alt="image" src="https://github.com/user-attachments/assets/eb87edd4-1e56-4960-b98c-b6dcc4772c4a" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1208" height="1100" alt="image" src="https://github.com/user-attachments/assets/64af765b-2313-4672-a428-24d768352988" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1618" height="1100" alt="image" src="https://github.com/user-attachments/assets/99f0717a-e7fb-4194-8495-55a15e940f86" />


tar -xvf backup.tar
## OUTPUT
<img width="741" height="76" alt="image" src="https://github.com/user-attachments/assets/d2b9dac5-02dd-484d-9af5-e74acb8f3d2b" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="804" height="276" alt="image" src="https://github.com/user-attachments/assets/8ffb01ec-052b-4264-a0fd-31cbfcdfa3da" />


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
<img width="799" height="41" alt="image" src="https://github.com/user-attachments/assets/6ad5c0ab-601f-40a4-a526-ecb1da8667d0" />

 
ls file1
## OUTPUT

<img width="799" height="41" alt="image" src="https://github.com/user-attachments/assets/789c25be-4f63-4f53-8739-d8c4ac7b7d07" />


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
<img width="538" height="209" alt="image" src="https://github.com/user-attachments/assets/553f5e3a-9421-4e4a-8d75-e7d5f496c03d" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="505" height="52" alt="image" src="https://github.com/user-attachments/assets/ab0577ca-7a5e-4dd5-933b-5333b8c0f816" />


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
<img width="505" height="52" alt="image" src="https://github.com/user-attachments/assets/606a668b-eae3-46bd-85f9-85ba785d665d" />

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
<img width="504" height="49" alt="image" src="https://github.com/user-attachments/assets/bf23c3da-cf4e-40be-9ac1-21f4a10357ad" />

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
<img width="519" height="63" alt="image" src="https://github.com/user-attachments/assets/2304e5c8-cb15-4332-8390-243ada0e37d6" />


# looking for a possible value using elif
cat > elifcheck.sh 
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
<img width="522" height="37" alt="image" src="https://github.com/user-attachments/assets/f4f2bf0d-bc3a-4fb4-a6a9-e1215141eddc" />


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
<img width="802" height="164" alt="image" src="https://github.com/user-attachments/assets/3962bfd3-d288-451a-bf2c-59c91c692089" />



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
<img width="799" height="203" alt="image" src="https://github.com/user-attachments/assets/5069d4e2-49ce-4669-9005-63351fe0e9f1" />


cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh$ ./forctype1.sh 
## OUTPUT
<img width="793" height="190" alt="image" src="https://github.com/user-attachments/assets/ae486c93-35d7-48ed-b37a-272b2395a2dd" />


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
 <img width="799" height="387" alt="image" src="https://github.com/user-attachments/assets/1a5bf6af-cabd-4d67-a2e3-40dfe9e29743" />


 
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
<img width="804" height="119" alt="image" src="https://github.com/user-attachments/assets/7f7b7446-45d3-4d6c-84d1-7f9ea84298ba" />


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
<img width="933" height="196" alt="image" src="https://github.com/user-attachments/assets/76503a80-b32f-487f-a410-1f2c37ed8eb8" />

 
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
<img width="764" height="124" alt="image" src="https://github.com/user-attachments/assets/2eb85308-866a-465b-9de2-7fdbe7b68b12" />



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="543" height="152" alt="image" src="https://github.com/user-attachments/assets/42a6d9aa-24a9-4896-b3e6-36dc82ac8274" />




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
<img width="422" height="124" alt="image" src="https://github.com/user-attachments/assets/619753ba-95f0-48d3-9473-5d336e26a88b" />

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
<img width="791" height="140" alt="image" src="https://github.com/user-attachments/assets/0a1b7e0e-3f39-4e97-8adc-4bba33c249e8" />

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
<img width="802" height="141" alt="image" src="https://github.com/user-attachments/assets/f7f8de55-67f9-45c5-b849-d054d67bf42a" />

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
<img width="792" height="443" alt="image" src="https://github.com/user-attachments/assets/c90cdc46-7502-4d39-8359-9857da0d39a7" />

 ./argshift.sh 1 2 3
 
 
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
<img width="776" height="433" alt="image" src="https://github.com/user-attachments/assets/e773487e-9d64-4d56-bfcd-d3887a34fa93" />

 
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
<img width="776" height="135" alt="image" src="https://github.com/user-attachments/assets/a8587073-556a-48c8-9dba-4adf522f8019" />



# RESULT:
The Commands are executed successfully.
