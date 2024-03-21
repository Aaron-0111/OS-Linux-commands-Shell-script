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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/b0c4d173-8eae-4ceb-b001-29d4d231384d)



cat < file2
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/872e9a55-0bc8-4d19-b3ea-e2ac24159081)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/a78faf1d-e2ed-4c08-bf23-5af0ec4a5002)

comm file1 file2
 ## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/6f05d623-21e4-4c49-9140-f4a6a8170f24)


 
diff file1 file2
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/39b268e9-9363-4fab-b651-7cf8d116c403)


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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/5098d43d-dba1-4268-afff-9f0456b6f9df)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/89c05978-9afd-4b1d-943c-44f8f0d2dbc4)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/e6630e17-6d0b-4d53-94d9-d065e657e26b)


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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/a44585f9-bfd4-442f-a991-289e5557833d)



grep hello newfile 
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/449ca30d-383a-4b21-b100-38a645b76627)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/6d74183f-a12b-4531-85bf-bee2552dea18)



cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/0f50adba-97d7-46a8-9415-e3c4452aac12)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/50dd0fca-6bf9-4992-ba95-7778dab736d8)



grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/0d3f9b77-c52e-40f1-a79a-febe622b7c69)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/93427219-b688-4f89-8639-3149bf464439)


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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/d57143d9-e289-4b3f-ae22-ea404644821c)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/3e927416-b783-4e3a-b661-e3f998af9a03)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/b18afeb7-4f24-4f66-9ec2-363431b3ffcf)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/77712644-dae1-4a67-8a30-c87d4fce5c9b)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/697f08b2-4dde-4a7a-bf49-f6cf084d0061)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/35bf7535-64db-4281-983b-97a9f42ad40b)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/6a72e461-051c-4b12-8016-26a5bf5d71bd)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/e0366d53-a983-4d2f-8945-7ca9e5918e2e)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/48c6562a-4dfe-4923-8bb1-bec018606c66)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/0e3da24a-f367-437c-b1ca-747f4172411a)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/5a1fd08f-d1e2-4c99-9cf7-9b84d9c0f241)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/7275359d-619f-46fa-a0ec-cbe39177e041)


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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/694fa445-5431-4cbe-ba19-319c28ac9810)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/a10580ed-2718-4edc-b0ed-f6ac21cdf7a7)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/46a90554-1f70-4131-8466-84b975f26a6c)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/5ecce101-d0bb-4eb0-b335-7b228248de6c)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/a66b88a3-9eea-4b77-8063-27249d06cdd1)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/584b285a-9ea6-44ca-be64-41d7173c2fc3)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/166f3b1f-2c7a-4497-9919-db73dffa5fdd)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/10d465fe-7a92-4bc2-8f35-ef39731be3cf)



seq 10 
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/5622a8d7-86c1-47b0-ac18-303565f68c7f)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/9d2277b0-8140-41fe-bf8d-c450305c359d)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/18b3d9df-107f-494c-937a-dbfdb803728a)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/47e86746-14aa-4371-ad3a-8e03b2e673b3)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/e741cf46-a218-444c-a5db-2afca8453d34)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/555802a1-08d1-4d7c-91d3-d0be43efddbd)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/49a8b0fe-b887-43b1-9ab4-b4b469b80de7)



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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/9b75d4cb-bebe-4782-b305-d2cfc348ffd4)


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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/3195c7a0-0b1a-4475-bcf3-0b32bb79ff45)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/024a70e1-889c-49a3-8fd8-e9c694a10c02)

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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/f40a78d2-b8e4-48d8-aaf4-475296731326)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/67379eed-ac50-46c3-b7d1-0d36cee7c6ca)



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/0a4ce841-e988-4ed3-9e0d-a3e81e74036b)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/46f9c93f-f97d-42ad-8503-40f2e8b199e3)


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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/2cda871a-8c58-4a08-ba3b-9c66d3499152)

echo $?
## OUTPUT 
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/8b202f54-3ad7-4e05-8e9a-1010706a6e15)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/7ff356ed-6776-4641-9927-8134a7b0d94e)

abcd
 
echo $?
 ## OUTPUT
1

 
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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/bbc2b033-20a5-45c2-a663-8788a9c8b00f)



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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/a00b80c8-16dc-4e70-96f4-bd228aa89463)



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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/caf7b921-c5c6-4092-853c-3fe6bc5d8868)

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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/44b50520-f929-46a2-9cd5-a68502ffa8db)

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
![image](https://github.com/Aaron-0111/OS-Linux-commands-Shell-script/assets/149347631/d6ba2deb-6ed9-4ef8-b253-1ee68ba1c878)

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
