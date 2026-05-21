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
<img width="351" height="109" alt="image" src="https://github.com/user-attachments/assets/402683ee-1763-41d8-89be-4853f670c081" />



cat < file2
## OUTPUT
<img width="345" height="126" alt="image" src="https://github.com/user-attachments/assets/90382809-1c56-46d9-8448-dd49c684d867" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="391" height="71" alt="Screenshot 2026-04-20 141701" src="https://github.com/user-attachments/assets/d5f00901-ef21-474c-ad21-b5379ab4520a" />

comm file1 file2
 ## OUTPUT
<img width="395" height="237" alt="Screenshot 2026-04-20 141731" src="https://github.com/user-attachments/assets/5aaf06f9-f130-4537-bf5d-456f70d6acef" />

 
diff file1 file2
## OUTPUT
<img width="474" height="280" alt="Screenshot 2026-04-20 141751" src="https://github.com/user-attachments/assets/d46683e1-f943-42f1-8033-5de7520845d4" />


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

<img width="345" height="126" alt="image" src="https://github.com/user-attachments/assets/183c171a-69f6-4c1b-b8ab-ccbdc08b4b5d" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="386" height="117" alt="Screenshot 2026-04-20 143317" src="https://github.com/user-attachments/assets/d631ba8c-b93c-419f-8109-1eb54eda8acb" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="489" height="110" alt="Screenshot 2026-04-20 143325" src="https://github.com/user-attachments/assets/a56cc835-b940-49e8-89a3-f9e40a4b7be7" />


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

<img width="435" height="62" alt="Screenshot 2026-04-20 143641" src="https://github.com/user-attachments/assets/e90f8f0d-dd8d-4edc-bb78-0509a092291b" />


grep hello newfile 
## OUTPUT
<img width="429" height="61" alt="Screenshot 2026-04-20 143703" src="https://github.com/user-attachments/assets/669a6a83-3ec1-444c-b24b-9360c69c13f1" />




grep -v hello newfile 
## OUTPUT

<img width="466" height="67" alt="Screenshot 2026-04-20 143846" src="https://github.com/user-attachments/assets/07707092-430c-4ba1-8921-5276e0fb3860" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="531" height="84" alt="Screenshot 2026-04-20 143912" src="https://github.com/user-attachments/assets/69012407-9870-4796-8025-00d45a48f8e1" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="743" height="60" alt="image" src="https://github.com/user-attachments/assets/888b13c3-5055-40c4-ba5b-933efa715b89" />



grep -R ubuntu /etc
## OUTPUT

<img width="820" height="573" alt="image" src="https://github.com/user-attachments/assets/ae2b0bd2-fa1f-444e-8026-31efb0ba4e2a" />


grep -w -n world newfile   
## OUTPUT
<img width="497" height="73" alt="image" src="https://github.com/user-attachments/assets/04ad1202-a0d8-450b-ae38-8cd09b2f7f16" />


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
<img width="587" height="84" alt="image" src="https://github.com/user-attachments/assets/acd7f8f0-befb-4d99-b1d7-c2a393a3d372" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="599" height="89" alt="image" src="https://github.com/user-attachments/assets/3e9176e3-b361-4a0c-ac8e-a5b1eca96d61" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="631" height="82" alt="image" src="https://github.com/user-attachments/assets/cf5bd6c5-585e-4b2e-ac3d-f36c6fc4f778" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="511" height="68" alt="image" src="https://github.com/user-attachments/assets/6767a57f-8686-462b-aad2-f3048d676da2" />


egrep '(world$)' newfile 
## OUTPUT

<img width="492" height="93" alt="image" src="https://github.com/user-attachments/assets/600abe59-5817-412b-bc3e-339563f620ea" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="553" height="60" alt="image" src="https://github.com/user-attachments/assets/12df17e0-846e-499d-979d-baa44e04dc1d" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="455" height="44" alt="image" src="https://github.com/user-attachments/assets/71491fbc-b22d-45f5-9899-31e227d61bf3" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="534" height="59" alt="image" src="https://github.com/user-attachments/assets/264c0733-7554-4e08-a853-07e262b4ccbe" />


egrep l{2} newfile
## OUTPUT
<img width="448" height="88" alt="image" src="https://github.com/user-attachments/assets/337b7e49-fb84-40e9-ad8f-deba914173a4" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="517" height="87" alt="image" src="https://github.com/user-attachments/assets/23bcc0df-59f2-4058-a1a3-a77d9c7a92ca" />


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
<img width="471" height="59" alt="image" src="https://github.com/user-attachments/assets/1ea97770-4e87-4868-bbea-5f3918eb5bde" />



sed -n -e '$p' file23
## OUTPUT

<img width="498" height="59" alt="image" src="https://github.com/user-attachments/assets/5cec3ad7-377b-4802-9c38-05cfc5e14db0" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="551" height="245" alt="image" src="https://github.com/user-attachments/assets/9a1f018b-ec2f-45e2-b20b-f8b80d3d36ed" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="751" height="241" alt="image" src="https://github.com/user-attachments/assets/ff2af3fc-2c9a-46ba-a1d6-872670494b6e" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="687" height="239" alt="image" src="https://github.com/user-attachments/assets/ba8714ef-ce75-4f65-b527-cb8e382b33cc" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="547" height="134" alt="image" src="https://github.com/user-attachments/assets/ea7b932b-7e90-4ee6-85ad-9617f9670e1c" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="687" height="127" alt="image" src="https://github.com/user-attachments/assets/be1b83c1-b421-45d6-b27e-db3c701ad026" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="588" height="64" alt="image" src="https://github.com/user-attachments/assets/fe4993b6-8010-422c-a487-d5ca3922e42c" />


seq 10 
## OUTPUT

<img width="428" height="260" alt="image" src="https://github.com/user-attachments/assets/c8fd0c84-fa1d-4f25-a7b9-d6ee8a1d543a" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="468" height="103" alt="image" src="https://github.com/user-attachments/assets/b52ec6b3-b030-4608-88e7-c7edb2b9f7e1" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="501" height="70" alt="image" src="https://github.com/user-attachments/assets/6b3558d6-9db7-4a34-a57a-0b660b226a89" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="539" height="106" alt="image" src="https://github.com/user-attachments/assets/b44ce032-8dd8-4b5c-985f-f0ee48ea87a6" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="508" height="90" alt="image" src="https://github.com/user-attachments/assets/085b0e02-2ade-445b-82f7-4ad22f048792" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="498" height="88" alt="image" src="https://github.com/user-attachments/assets/40e7a392-7e9d-4122-bada-612363264824" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="595" height="85" alt="image" src="https://github.com/user-attachments/assets/14069c72-fd2f-4e20-b427-3731319b74e2" />


sed -n '2,4{s/$/*/;p}' file23

<img width="719" height="102" alt="image" src="https://github.com/user-attachments/assets/b9ffd196-876f-4bf3-ba60-0e618a34cf40" />

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
<img width="355" height="108" alt="image" src="https://github.com/user-attachments/assets/1114018a-6430-4951-a007-0a263b33fc0f" />


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

<img width="376" height="124" alt="image" src="https://github.com/user-attachments/assets/a192004a-ab81-4bbe-8247-aed469dfadf2" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="771" height="238" alt="image" src="https://github.com/user-attachments/assets/3df4c356-4fd4-4a83-b1ca-10f82ae862fa" />

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

<img width="536" height="86" alt="image" src="https://github.com/user-attachments/assets/ff2fe0ef-984b-4544-95a1-5954a7061745" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="665" height="84" alt="image" src="https://github.com/user-attachments/assets/dfb3867d-1ae9-46f3-a1c5-21414f6ecc29" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="463" height="194" alt="image" src="https://github.com/user-attachments/assets/e6c5bf18-f285-4bb8-b3d1-e0d9feb03774" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="728" height="197" alt="image" src="https://github.com/user-attachments/assets/5c359fc2-362a-40c7-b5c4-d35a13fd7797" />

tar -xvf backup.tar
## OUTPUT
<img width="464" height="183" alt="image" src="https://github.com/user-attachments/assets/85ad7857-e39a-4429-a935-9db2c7be8ac6" />



 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="412" height="90" alt="image" src="https://github.com/user-attachments/assets/21c71193-5ef8-45b3-9c5c-a3ff4bfd6256" />


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
<img width="527" height="259" alt="image" src="https://github.com/user-attachments/assets/0c93a0b1-c123-4274-9180-6f2f3f6f52d3" />

 
ls file1
## OUTPUT
<img width="333" height="65" alt="image" src="https://github.com/user-attachments/assets/1fe40fc6-1b6f-4485-aa0e-40ebd92e4b47" />

echo $?
## OUTPUT
<img width="343" height="64" alt="image" src="https://github.com/user-attachments/assets/30b03103-7b1f-429e-a41b-4f01e00b6fe1" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="343" height="64" alt="image" src="https://github.com/user-attachments/assets/ae532eda-9bea-465d-88e9-f90acfba5dc5" />

abcd
 
echo $?
 ## OUTPUT
<img width="343" height="64" alt="image" src="https://github.com/user-attachments/assets/a0c98d13-9684-4dd8-a6a7-e87206dd79cf" />


 
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
<img width="725" height="216" alt="image" src="https://github.com/user-attachments/assets/91abfe30-3b31-4096-b28d-361b836088be" />




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
