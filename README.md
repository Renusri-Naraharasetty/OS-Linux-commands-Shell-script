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
# DISPLAY THE CONTENT OF THE FILES
cat < file1
## OUTPUT:
![image](https://github.com/user-attachments/assets/2d77b858-ea47-4b60-8f8f-646564ce8888)


cat < file2
## OUTPUT:
![image](https://github.com/user-attachments/assets/849d1ce5-b38b-469b-8786-6ca55db873db)



# COMPARING FILES
cmp file1 file2
## OUTPUT:
![image](https://github.com/user-attachments/assets/ae108a8b-f484-4aa4-83c5-9287fd8a4cb3)


 
comm file1 file2
## OUTPUT:
![image](https://github.com/user-attachments/assets/e9266811-4c8a-42d1-a0a8-1404f78d862e)



diff file1 file2
## OUTPUT:
![image](https://github.com/user-attachments/assets/a024cfbb-09e0-4f71-862f-475cc6983dd1)




# Filters

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
## OUTPUT:
![image](https://github.com/user-attachments/assets/5f78084e-4216-4d2f-9eaa-f9db2046d8e4)


cut -d "|" -f 1 file22
## OUTPUT:
![image](https://github.com/user-attachments/assets/f9d7323d-42f3-4011-bae5-94b8a11e710a)


cut -d "|" -f 2 file22
## OUTPUT:
![image](https://github.com/user-attachments/assets/bc13df8d-b9ba-4db3-88b2-3287b4725eac)




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
## OUTPUT:
![image](https://github.com/user-attachments/assets/f84c4a43-d0fd-4585-b39c-11ac6b174d53)



grep hello newfile 
## OUTPUT:
![image](https://github.com/user-attachments/assets/53294344-b7be-4af0-8c3e-a81e44e77a1a)



grep -v hello newfile 
## OUTPUT:
![image](https://github.com/user-attachments/assets/15ac7b4e-45c4-4bce-a3c9-1d35c06d515f)



cat newfile | grep -i "hello"
## OUTPUT:
![image](https://github.com/user-attachments/assets/cfbbac96-bc09-4829-a97b-d5fc496bc308)



cat newfile | grep -i -c "hello"
## OUTPUT:
![image](https://github.com/user-attachments/assets/f01cfb88-3378-4ead-8812-7ab81c312acc)



grep -w -n world newfile   
## OUTPUT:
![image](https://github.com/user-attachments/assets/2e2acd1c-b43d-4b65-8e8c-23dc0738fde0)



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
## OUTPUT:
![image](https://github.com/user-attachments/assets/7b36b866-bbbc-47e9-bab4-35cb9f42d3e4)



egrep -w '(H|h)ello' newfile 
## OUTPUT:
![image](https://github.com/user-attachments/assets/fcdd9f2f-b703-4960-98c3-bff3b1363caa)




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT:
![image](https://github.com/user-attachments/assets/917db146-55e7-472c-ad00-f874e7ca1198)



egrep '(^hello)' newfile 
## OUTPUT:
![image](https://github.com/user-attachments/assets/649f1eeb-d0f5-49a0-ac27-c9ec3aa9f5c6)




egrep '(world$)' newfile 
## OUTPUT:
![image](https://github.com/user-attachments/assets/2fde1e8e-d540-48c6-bcf4-9d3c91ce77b3)



egrep '((W|w)orld$)' newfile 
## OUTPUT:
![image](https://github.com/user-attachments/assets/9f601fd4-5f6e-4eb9-9e2b-ff911b855b19)




egrep '[1-9]' newfile 
## OUTPUT:
![image](https://github.com/user-attachments/assets/eb598123-db9f-481e-8b61-cdbd610fc867)




egrep 'Linux.*world' newfile 
## OUTPUT:
![image](https://github.com/user-attachments/assets/140ba11d-221f-45a2-8dbb-96163a4cbc99)



egrep l{2} newfile
## OUTPUT:
![image](https://github.com/user-attachments/assets/ba2dc1b7-c4f2-471b-a2d1-aa5e546601c9)




egrep 's{1,2}' newfile
## OUTPUT:
![image](https://github.com/user-attachments/assets/8cc12b1c-eac4-41db-a550-d998d93d3a94)



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
## OUTPUT:
![image](https://github.com/user-attachments/assets/b70ae39e-4bce-40c0-b2b2-2d4a3fb8c55e)




sed -n -e '$p' file23
## OUTPUT:
![image](https://github.com/user-attachments/assets/657644d8-cb76-4895-a683-ebb491ceb36e)




sed  -e 's/Ram/Sita/' file23
## OUTPUT:
![image](https://github.com/user-attachments/assets/9ae34194-a842-48cd-89c3-1750ef5f3dae)




sed  -e '2s/Ram/Sita/' file23
## OUTPUT:
![image](https://github.com/user-attachments/assets/326de367-c79b-45f7-a362-b073a88ce9cf)




sed  '/tom/s/5000/6000/' file23
## OUTPUT:
![image](https://github.com/user-attachments/assets/2ed2d541-06c6-4f36-b9e7-dcf84df9b279)




sed -n -e '1,5p' file23
## OUTPUT:
![image](https://github.com/user-attachments/assets/6c636d02-6bb6-444b-84ba-f1d6f5a3e2cd)




sed -n -e '2,/Joe/p' file23
## OUTPUT:
![image](https://github.com/user-attachments/assets/c0ae829b-84b8-4c38-9aba-27ea1064c899)





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT:
![image](https://github.com/user-attachments/assets/98344db6-9a50-492a-89fd-b765f1ac7b24)




seq 10 
## OUTPUT:
![image](https://github.com/user-attachments/assets/c3faed05-e1e6-4628-8fea-744c897fa8d1)




seq 10 | sed -n '4,6p'
## OUTPUT:
![image](https://github.com/user-attachments/assets/8276a805-128c-424d-beaa-acc5bcf49496)




seq 10 | sed -n '2,~4p'
## OUTPUT:
![image](https://github.com/user-attachments/assets/96cd7fcd-aff2-4c5c-99a0-823108ffdd6a)




seq 3 | sed '2a hello'
## OUTPUT:
![image](https://github.com/user-attachments/assets/5221e573-1ad7-430c-b79a-ed8547ac58ca)




seq 2 | sed '2i hello'
## OUTPUT:
![image](https://github.com/user-attachments/assets/aa7e56e8-6d3b-4035-817a-3fb23cd3922e)



seq 10 | sed '2,9c hello'
## OUTPUT:
![image](https://github.com/user-attachments/assets/cdfd8069-a08c-443b-943c-96123fba7203)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT:
![image](https://github.com/user-attachments/assets/64326568-1f59-426d-aa7d-63058ad0eded)




sed -n '2,4{s/$/*/;p}' file23
## OUTPUT:
![image](https://github.com/user-attachments/assets/42088774-fc42-4a79-bf45-eb5a96813383)



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
## OUTPUT:
![image](https://github.com/user-attachments/assets/9e6f7695-4d62-4057-9139-2f22a42224ed)



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
## OUTPUT:
![image](https://github.com/user-attachments/assets/aa44ea24-7ce5-4051-82fd-c7eb40790138)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT:
 ![image](https://github.com/user-attachments/assets/c570a6ce-f582-47c3-bbfa-c9c927ccb98f)


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
 ## OUTPUT:
 ![image](https://github.com/user-attachments/assets/842c6567-761c-46fa-b675-17c70fee34a8)



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT:
![image](https://github.com/user-attachments/assets/8ef2e235-d5c5-41dc-9078-f5d9fd7d7090)




#Backup commands
tar -cvf backup.tar *
## OUTPUT:
![image](https://github.com/user-attachments/assets/96631275-784e-4779-8f47-fe04825640c0)



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT:
```
-rw-r--r-- user/group 0 2024-02-25 14:30:00 file1.txt
drwxr-xr-x user/group 0 2024-02-25 14:30:00 directory1/
-rw-r--r-- user/group 1024 2024-02-25 14:30:00 directory1/file2.txt
-rw-r--r-- user/group 2048 2024-02-25 14:30:00 directory1/file3.txt
```



tar -xvf backup.tar
## OUTPUT:
```
x file1.txt
x directory1/
x directory1/file2.txt
x directory1/file3.txt
```

gzip backup.tar

ls .gz
## OUTPUT:
```
 backup.tar.gz
```
 
gunzip backup.tar.gz
## OUTPUT:
```
backup.tar
```

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT:
![image](https://github.com/user-attachments/assets/90198888-be6e-4326-9f75-f157ba4120cb)


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT:
![image](https://github.com/user-attachments/assets/f723a2ba-373e-4709-a259-b19bfc27bccb)



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

## OUTPUT:
![image](https://github.com/user-attachments/assets/6c5ae25d-4c84-4f80-abfa-79188d72b443)


 
ls file1
## OUTPUT:
![image](https://github.com/user-attachments/assets/da5f5d65-7e88-4576-8fef-5c0ec63a7510)


echo $?
## OUTPUT:
![image](https://github.com/user-attachments/assets/8b510106-5b6f-4f28-860c-297399a64687)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT:
![image](https://github.com/user-attachments/assets/24e89db2-26ef-4d82-891e-231740661a42)

 
abcd
 
echo $?
 ## OUTPUT:
 ![Uploading image.png…]()



 
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
