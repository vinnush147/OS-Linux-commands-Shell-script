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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/d5e33df0-631a-4485-8f75-2b4753619efc)


cat < file2
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/324ded96-7434-419e-bc32-268407b50b33)

# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/c39a4f46-d68f-4cde-a18e-9731e2606be1)
 
comm file1 file2
 ## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/aca84cad-f6da-41a8-a4bb-95035598ffcb)
 
diff file1 file2
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/89c52a2b-0a93-40c7-97f3-a186bc7c1e51)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/3430c44c-704b-47e0-83a1-ab6fe2964f0e)


cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/07d9e46b-ef75-46e1-81c2-c8f43ec4b50a)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/3e7a108a-5318-4f86-af7f-028b427d9307)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/63d0b2da-d539-433f-a2e2-5ce539c66d74)


grep hello newfile 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/ca155fec-952a-45c9-9d0d-e32491b5c837)

grep -v hello newfile 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/f72a578f-a9b1-49ca-b5cc-4865aeb29b7e)

cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/7445f3c7-7ce2-4fd6-8d7f-a9d07ac07e4b)

cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/27a11695-e895-463d-8ffd-efb6f2be53df)

grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/f4242e73-ae98-46ae-aa53-5309497154ee)
![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/45bf4fe2-f4dc-4ab2-bc7a-a31edecfb53e)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/3a88d3f9-6681-4396-b04e-7a419ae81d91)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/e535e943-789f-4181-a31c-81396b07dd7e)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/1a09a868-1a26-491b-b33c-6f850bf9fb01)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/fa3a24fb-3f2d-41f6-87c5-17cf46c2fcd5)

egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/4d925a7e-b5bc-48c7-9663-28c7d9c0af4c)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/5b0436f9-ff03-4814-ba60-5d234bc23bcb)

egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/47a225dc-863d-44e4-85d2-515cdc71f4e6)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/767dea3e-c631-4f94-87f1-dddc08832fd4)

egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/81ddae9d-8465-4974-89c6-43c8da12e14e)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/ef419f24-0956-4d43-a217-8626d81f0d14)

egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/89c40058-1273-4c3f-b13d-805a4f2f4325)

egrep l{2} newfile
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/653567fb-b930-4408-8831-864ee4501c7e)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/22fd3562-c824-4b34-b7ae-0be59f415a30)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/68c50fdd-37b7-4cbf-92b4-2eef41b2b1b8)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/8b2a0093-a315-4338-9500-74a3bf7a80d0)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/e853adb8-edc2-4689-b84b-0657a177b2f9)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/31fd034f-54c7-4b0d-b480-4c28ccd658f4)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/e64cd89d-da6b-444c-81de-eab704f98951)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/68fde2b4-c082-411e-9ac7-7fb212006f30)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/8ae734fd-cac0-4e2f-909e-92458d7a6a06)

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/00320302-47f1-458a-811d-63e44a06ef21)

seq 10 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/669c950b-4a5c-4cd0-90c2-2e352bebe86c)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/c0a89806-fb6c-4c90-a488-08b8d1630f37)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/c421b40b-7fc1-4acc-851c-38972c1d8178)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/1d6e4455-3e88-4c55-86ca-58096ed71cd0)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/32e4f1ed-fda5-4178-90c4-62bf39984055)

seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/b4d40528-0064-481c-b8d2-2d760ccb4340)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/96820231-15ac-45ef-861e-a7820eaaaa81)


sed -n '2,4{s/$/*/;p}' file23

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/e8ae391c-55d7-4550-aada-683102c1edd0)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/7667d968-4f4e-413b-b42a-6d8cfbf7ec51)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/687973f7-cadd-423b-b876-80b6a30cd4cc)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/c6d3bfae-dad1-403e-ac03-ffc4e144f9a5)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/c170d02e-1a5b-4748-9249-4ead95ce6a1d)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/4d430692-491c-4d64-8c90-34ce1f4d1587)

#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/41594c40-8496-4957-a300-01269991e43e)
![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/b7918340-5491-4860-8a01-667470561e5e)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/de9e09d3-b35a-4015-896e-a26444102ceb)

tar -xvf backup.tar
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/d6c7ad1c-d105-4004-aa4e-1fb9f9ffca79)

gzip backup.tar

ls .gz
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/d2278136-7d4a-4876-8be0-4be4bb4c62d2)
 
gunzip backup.tar.gz
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/79fc1efd-501e-4fe9-84b5-a414f56c4623)
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/bd59ef41-1a9d-4f53-80de-846c3cda2819)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/e23e74d4-7cd1-4247-b0aa-c672ecb8bdb1)


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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/595d3d66-a67a-4378-a861-92bf464db6b5)
 
ls file1
## OUTPUT
![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/c6969d25-4a2a-4cbf-848e-85c24fd9fea4)

echo $?
## OUTPUT 
![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/ad838fa3-8dd8-4126-8c41-e2c20d99df27)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/f8110307-12cc-4015-bed2-677c044ce691)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/20d9ffb7-4a94-4ddb-be34-35001e8f0861)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/a45036c6-174f-4861-8061-7640a89f8304)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/3cc9c834-1afa-4c56-aa4a-d8589d725ceb)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/45790913-9f03-4f5a-983c-c735858d4cee)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/e2772958-3837-47ae-9e09-18c2eaf2c074)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/ce516d27-7ebe-4ff2-a1c9-1f973cb073c0)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/69decc6a-c825-486a-951f-5a85fc0053bb)

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
 
![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/a3f2f951-56ce-402c-9ed2-2e3e8c8c4f07)

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
 
![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/e1248027-7165-4d28-a4da-8393b089fd55)

 
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
 
![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/d2d5e00a-4c73-42b5-ab35-abffd8c01244)
 
 
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
 
![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/70e66845-7f5b-4430-949f-2e834b551a16)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/92079961-33db-41a1-a7ab-b57a0f981607)
 
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

 ![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/e5256de7-ca7a-4218-82bd-f88847887991)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/2fb62dc5-87af-4ddf-b34b-b6d65a06f376)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/cbafeaa2-c217-4f90-8e4b-bd1b53eaad6d)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/a388c479-eb98-4ab0-83af-917af660adf4)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/215b8323-2c06-4454-bfe1-f82432ee86a7)
 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/95b84552-aa0f-4ef4-b3bb-f30474a2cf25)
 
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

![WhatsApp Image 2024-02-26 at 13 37 43_abfc4b93](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/01d71770-1fd2-484b-b6d1-e85a03386acc)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

$ ./exread1.sh 

![WhatsApp Image 2024-02-26 at 13 37 43_abfc4b93](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/d01e4d8b-8a81-4b52-8f84-0abcc6d9f3db)
 
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

  ./funcex.sh 1 2

 ![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/94e040c6-eaca-4e6c-a22a-e32b243319c0)

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
$ ./argshift.sh 1 2 3

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/87d49c52-0d2e-4132-bdeb-a6a72407dcae)
 
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

 ![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/5b68393d-3fc8-4a7e-9b4c-db1c4cff7a09)

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
 
 ![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/e620c3a9-de08-4cc4-b200-6fbdc0f41c7a)

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

 ![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/0828beb9-d21a-4b6a-aea3-efae2a501628)

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

![image](https://github.com/dharshini-29/OS-Linux-commands-Shell-script/assets/147474632/5b86b486-cd91-40c2-a715-137a2a1a071f)

# RESULT:
The Commands are executed successfully.
