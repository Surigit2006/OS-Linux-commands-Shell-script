yyOperating systems Lab exercise
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
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/887ab41f-3374-4c21-af38-633e5f13f592" />




cat < file2
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/0e1cdcf3-e131-4065-89fc-4fa6031edd05" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/9a5eca20-421a-4e00-8f88-b152d0e4b56b" />

comm file1 file2
 ## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/f5168e68-79fd-4c38-b911-33ab8211dc85" />

 
diff file1 file2
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/8790900e-e610-4286-95b5-bcfb6c8a32eb" />


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
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/0604a270-0808-42c1-b9ca-a1040e1b5452" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/69e82f33-176d-4c3b-8ee3-f2b76e1afd6d" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/281b8f79-638f-4ba7-884e-64e3ab105d4e" />


cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/e84f29ac-c723-47ed-b9f5-93a6abc4dd18" />



grep hello newfile 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/df2bba88-15d2-4f55-94c2-4d9f060aab40" />




grep -v hello newfile 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/8603784b-d77d-431f-b72e-877415d53106" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/7f084a95-d6da-4807-831d-97bdb19487fd" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/63acf31b-190a-4025-9e8c-4e8ccc96348f" />




grep -R ubuntu /etc
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/6b59ca71-d701-43a4-aeb7-74b83534690f" />




grep -w -n world newfile   
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/a15ba7df-ed4a-4f69-9858-95b6714f650a" />



cat > newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat < newfile
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
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/f1590a16-230e-403d-bb0a-969efd2f9886" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/89e510c9-e4f2-4f68-8552-3df33f8f0c91" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/93d7c596-4fc4-4f6b-8651-51eb4269f276" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/40462ead-cc2e-4fe4-aa8c-0a45c1c049aa" />



egrep '(world$)' newfile 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/24128074-2277-4cf4-aa04-2ffdb1514f28" />



egrep '(World$)' newfile 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/839687d3-6f6b-4881-ae06-04f4f7bc1fb0" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/aaa2f745-ec71-493e-99a7-f792ce6cbcd4" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/4f95ff55-cd61-419a-8770-3732b7b8cdea" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/3cc2c8f8-e322-4677-9468-68dfe503cfe2" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/8b8e9693-9fc7-4bee-bfc9-9acb83f228b6" />


egrep l{2} newfile
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/67669aff-6220-4e3a-b084-ba79d01899f1" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/e8de9eff-bbda-4b5f-92c2-8a2abf34314a" />


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
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/81d3597e-94be-474c-8b17-c048e1d2e9f9" />



sed -n -e '$p' file23
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/9f66a5c3-a504-4aa4-aa65-f8b9536e37ba" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/3d205ab9-8397-4ab2-aabe-98a448b29cb2" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/1f42a5b6-8450-4643-b7a4-78f28f5d65b4" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/fa3d3758-ec2e-4e70-9ac7-e65f09b3d62f" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/9a9fd452-2bf4-4531-9f47-5fa228d31c8b" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/ba377a2c-f3a3-47cc-8b7b-bde1670035cd" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/b3716684-24d2-455d-a429-4a9f76308d51" />



seq 10 
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/e2f56511-dc15-4f02-a3bc-f3c74e6b0192" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/ed9ee4dd-d517-4fb6-8567-a71e7848e23a" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/db7c1ad9-4c63-456a-af43-3f30671dc512" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/c03c8156-575c-4fd5-b545-ba828909c797" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/dcbf002b-9bb4-47d4-b4a5-7d2849ab807e" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/3c72339f-0deb-4d12-b7d2-1abb602cb771" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/9dde6b1f-3d0f-4347-9746-49ebc3922fe3" />



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
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/d399276a-9d28-4c0c-9e9e-2f092d0478be" />


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
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/a5684d23-eb26-4ad1-9126-234bc638044e" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/a90e4d14-23fb-4139-8127-8516497401a2" />

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/a21a56ec-1b52-4132-a44e-c509bb2cfa4c" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/9729a940-13da-4dfd-a1eb-b2ca342dd7c3" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/4ebdc9a6-0f4e-4921-a3d0-7d262a2e405d" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/10752b05-cf55-4d10-b32b-f7b9040bb57c" />


tar -xvf backup.tar
## OUTPUT
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/f7a72cf4-32d6-402f-acb8-7f65266b4eea" />

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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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


# RESULT:
The Commands are executed successfully.
