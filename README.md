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
<img width="387" height="187" alt="Screenshot 2026-04-29 130646" src="https://github.com/user-attachments/assets/be5d7ff3-3214-4d20-970a-c1d56379eb3b" />



cat < file2
## OUTPUT
<img width="437" height="238" alt="image" src="https://github.com/user-attachments/assets/627aa434-cee4-4fa9-85b3-64a75d571e42" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="540" height="129" alt="Screenshot 2026-04-29 130948" src="https://github.com/user-attachments/assets/66e9e55e-fb27-4ec3-84c3-3908aae2b9cc" />

comm file1 file2
 ## OUTPUT
<img width="381" height="267" alt="Screenshot 2026-04-29 131041" src="https://github.com/user-attachments/assets/39315fa9-6c13-43a0-880c-fe00e4925f4d" />

 
diff file1 file2
## OUTPUT
<img width="404" height="317" alt="Screenshot 2026-04-29 131124" src="https://github.com/user-attachments/assets/720b9991-d60d-4424-9842-693df742af80" />


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
<img width="360" height="174" alt="Screenshot 2026-04-29 131555" src="https://github.com/user-attachments/assets/3608195a-8b40-4b15-a234-cb41091e001f" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="394" height="176" alt="Screenshot 2026-04-29 131651" src="https://github.com/user-attachments/assets/dfa70696-a2b2-42b3-a77c-43ba64f8bde6" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="433" height="165" alt="Screenshot 2026-04-29 131727" src="https://github.com/user-attachments/assets/284f8626-f673-4d9c-ad5b-55cfbd9363e0" />


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
<img width="401" height="147" alt="Screenshot 2026-04-29 132022" src="https://github.com/user-attachments/assets/b8c841d4-d738-4ad8-9c27-6c93bbe42518" />



grep hello newfile 
## OUTPUT

<img width="401" height="147" alt="Screenshot 2026-04-29 132022" src="https://github.com/user-attachments/assets/3f00aa23-b027-46e5-aac4-798ef42525a4" />



grep -v hello newfile 
## OUTPUT

<img width="398" height="96" alt="Screenshot 2026-04-29 132123" src="https://github.com/user-attachments/assets/da8a8d82-8184-4f45-a55b-0b54fec7bce5" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="444" height="153" alt="Screenshot 2026-04-29 132209" src="https://github.com/user-attachments/assets/f5283990-2393-4607-8213-495c589d859e" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="470" height="129" alt="Screenshot 2026-04-29 132244" src="https://github.com/user-attachments/assets/a49fd9a9-c9e2-4ac6-8058-60090e772463" />




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="406" height="127" alt="Screenshot 2026-04-29 132415" src="https://github.com/user-attachments/assets/a6eb4327-64f9-45ef-a053-a765c427b656" />


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
<img width="480" height="149" alt="Screenshot 2026-04-29 132654" src="https://github.com/user-attachments/assets/0c45e1d1-e950-4e1e-beb8-a37a64055c83" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="466" height="143" alt="Screenshot 2026-04-29 132740" src="https://github.com/user-attachments/assets/de2ec146-d46e-4fe8-a4a9-f6d49571dbee" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="452" height="151" alt="Screenshot 2026-04-29 132839" src="https://github.com/user-attachments/assets/c88d1e36-3c61-4855-b4ef-7c7185c26ce9" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="432" height="123" alt="Screenshot 2026-04-29 132946" src="https://github.com/user-attachments/assets/0417be80-d04b-4023-a17b-292211c606e1" />



egrep '(world$)' newfile 
## OUTPUT
<img width="532" height="149" alt="Screenshot 2026-04-29 133039" src="https://github.com/user-attachments/assets/463597ea-f66a-4e12-b8ed-e57e5a4d5c67" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="435" height="130" alt="Screenshot 2026-04-29 133354" src="https://github.com/user-attachments/assets/b1e90b3c-c765-47d5-a055-709d2b28e2df" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="309" height="103" alt="Screenshot 2026-04-30 071404" src="https://github.com/user-attachments/assets/3b02e76e-b03c-4bb5-8486-31df379f0e73" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="372" height="99" alt="Screenshot 2026-04-30 071416" src="https://github.com/user-attachments/assets/2da70a4f-cda1-4884-9b6b-606cee932b80" />


egrep l{2} newfile
## OUTPUT



egrep 's{1,2}' newfile
## OUTPUT 
<img width="407" height="200" alt="Screenshot 2026-04-30 071524" src="https://github.com/user-attachments/assets/4c143321-123e-41f4-8504-d8734b46fa80" />


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

<img width="431" height="136" alt="Screenshot 2026-04-29 134341" src="https://github.com/user-attachments/assets/f9c7a17f-9e18-408d-ba6a-4959ba15a56d" />



sed -n -e '$p' file23
## OUTPUT

<img width="581" height="126" alt="Screenshot 2026-04-29 134430" src="https://github.com/user-attachments/assets/f08cb5f9-8de8-41f3-971c-126bcd695233" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="480" height="308" alt="Screenshot 2026-04-29 134513" src="https://github.com/user-attachments/assets/63e1d7db-ea70-47e8-9090-09c508e44869" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="470" height="308" alt="Screenshot 2026-04-29 134621" src="https://github.com/user-attachments/assets/88acdfd9-d05f-4395-a003-5c0c941d8c02" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="438" height="298" alt="Screenshot 2026-04-29 134709" src="https://github.com/user-attachments/assets/5cf5502c-8dd4-4ff0-8c81-b752a79881d7" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="410" height="228" alt="Screenshot 2026-04-29 134741" src="https://github.com/user-attachments/assets/44ce86c6-adeb-4b60-bbad-313e71995e2a" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="385" height="169" alt="Screenshot 2026-04-29 134811" src="https://github.com/user-attachments/assets/f830ee66-78ef-4775-afe8-e39d0a457450" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="458" height="147" alt="Screenshot 2026-04-29 134848" src="https://github.com/user-attachments/assets/0fb45d18-8375-4941-804c-2269c8a6b3df" />



seq 10 
## OUTPUT

<img width="350" height="336" alt="Screenshot 2026-04-29 134908" src="https://github.com/user-attachments/assets/62a5422e-41f6-436a-a69f-5fa7de21511f" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="378" height="177" alt="Screenshot 2026-04-29 134934" src="https://github.com/user-attachments/assets/78bd8fea-c5af-4909-81ff-ef8f56821d39" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="506" height="117" alt="Screenshot 2026-04-30 071848" src="https://github.com/user-attachments/assets/bfef559a-66e0-4018-ac43-fe472658bebb" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="551" height="152" alt="Screenshot 2026-04-30 071855" src="https://github.com/user-attachments/assets/e1260f8d-e59a-46de-a428-a9e7edb9be38" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="561" height="184" alt="image" src="https://github.com/user-attachments/assets/bf8fe098-c762-42c7-884a-97e709b9536e" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="500" height="180" alt="image" src="https://github.com/user-attachments/assets/abb3a577-110f-41aa-8e09-3eeb0e1fb06e" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="546" height="162" alt="image" src="https://github.com/user-attachments/assets/0ff0494e-4b5c-4096-a5b3-3f95c15f849d" />



sed -n '2,4{s/$/*/;p}' file23

<img width="592" height="187" alt="image" src="https://github.com/user-attachments/assets/189aa5e8-fb32-4a26-a5f5-352359b5a2a5" />


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

<img width="417" height="228" alt="Screenshot 2026-04-29 135721" src="https://github.com/user-attachments/assets/df62d04e-42ed-462d-87f7-8bb5dd440932" />


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

<img width="376" height="223" alt="Screenshot 2026-04-29 135955" src="https://github.com/user-attachments/assets/296e884c-a81d-474c-a650-5e19bf273081" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="476" height="296" alt="Screenshot 2026-04-29 140046" src="https://github.com/user-attachments/assets/34b656f6-af64-4500-91f3-d763cd579523" />

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

<img width="411" height="176" alt="Screenshot 2026-04-29 140308" src="https://github.com/user-attachments/assets/c94362cf-2bd4-4cb8-adaf-ea6b36f412a5" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="521" height="172" alt="Screenshot 2026-04-29 140400" src="https://github.com/user-attachments/assets/5bf68855-2e78-4234-9b3c-06a86308a5ce" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="463" height="186" alt="Screenshot 2026-04-30 072634" src="https://github.com/user-attachments/assets/79153354-cf91-4986-b756-e04fd9213f0b" />


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
<img width="621" height="496" alt="Screenshot 2026-04-30 073421" src="https://github.com/user-attachments/assets/2f546845-85ac-485a-9a43-be7b24c79ddc" />

 
ls file1
## OUTPUT

<img width="540" height="75" alt="Screenshot 2026-04-29 201613" src="https://github.com/user-attachments/assets/4e89880b-f10b-40a4-82b4-ef57a8c39b4d" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

<img width="359" height="80" alt="Screenshot 2026-04-29 201619" src="https://github.com/user-attachments/assets/bf4aea77-056b-4060-8298-19532df526c2" />
 
echo $?
## OUTPUT 

<img width="434" height="83" alt="Screenshot 2026-04-29 201727" src="https://github.com/user-attachments/assets/eb7b289e-18e1-471d-b635-ec51e1353a12" />
 
abcd
 
echo $?
 ## OUTPUT

<img width="434" height="83" alt="Screenshot 2026-04-29 201727" src="https://github.com/user-attachments/assets/9ae14d6e-a958-4e67-840a-b6edfa75f3f4" />


 
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
<img width="638" height="253" alt="Screenshot 2026-04-30 073823" src="https://github.com/user-attachments/assets/7d8d14ae-940b-4635-867f-af2aab2afea4" />

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

<img width="552" height="617" alt="Screenshot 2026-04-29 202700" src="https://github.com/user-attachments/assets/f566ba51-a441-44fe-8b50-742721eba01e" />



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

<img width="564" height="602" alt="Screenshot 2026-04-29 203158" src="https://github.com/user-attachments/assets/308d3d39-ac83-4983-98ee-2729c4639fb5" />

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


<img width="552" height="617" alt="Screenshot 2026-04-29 202700" src="https://github.com/user-attachments/assets/6c8839ba-5c0e-4c1a-adb5-0a6dab9c3485" />


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

<img width="694" height="423" alt="Screenshot 2026-04-29 205258" src="https://github.com/user-attachments/assets/801d3cc7-574e-48bf-8edb-1973a5b44a8a" />

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
##outout:

<img width="692" height="497" alt="Screenshot 2026-04-29 205735" src="https://github.com/user-attachments/assets/c54fba48-fc3f-4316-af8b-33d2e250174f" />

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

<img width="717" height="598" alt="Screenshot 2026-04-29 210212" src="https://github.com/user-attachments/assets/e2f0d25a-3cc4-46d6-becc-a92b0de1eb92" />
 
 
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

 <img width="590" height="507" alt="Screenshot 2026-04-29 210538" src="https://github.com/user-attachments/assets/8bbdf0ea-e87e-4a40-adf4-ed4ec79a7066" />

 
 
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

 <img width="694" height="542" alt="Screenshot 2026-04-29 210909" src="https://github.com/user-attachments/assets/3d210ae0-d156-4707-b5ed-dc38314adeb1" />

 
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

<img width="738" height="543" alt="Screenshot 2026-04-29 211222" src="https://github.com/user-attachments/assets/240a16fa-c227-49f8-99c0-eec35dfeb95a" />
 
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
<img width="694" height="542" alt="Screenshot 2026-04-29 210909" src="https://github.com/user-attachments/assets/8239b8fc-01c2-4749-8d01-bb3671a17a41" />

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

<img width="738" height="543" alt="Screenshot 2026-04-29 211222" src="https://github.com/user-attachments/assets/ffe16476-2660-4d5d-a0e8-0d8537f8f558" />

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
<img width="603" height="207" alt="Screenshot 2026-04-30 075918" src="https://github.com/user-attachments/assets/08dd07cd-2515-4a11-af60-002a78a71167" />



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
<img width="614" height="547" alt="Screenshot 2026-04-30 080253" src="https://github.com/user-attachments/assets/7534706d-5da0-4ca9-a642-5cbca6892edf" />

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
 <img width="539" height="535" alt="Screenshot 2026-04-30 080925" src="https://github.com/user-attachments/assets/07c47e72-a46f-4086-a0ed-2635344d0b22" />

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
<img width="496" height="481" alt="Screenshot 2026-04-30 080510" src="https://github.com/user-attachments/assets/9de4ffd3-9485-460e-acc3-110f8035cbf6" />

 
 
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
 <img width="522" height="431" alt="Screenshot 2026-04-30 081447" src="https://github.com/user-attachments/assets/caeec095-11f1-44f1-8a82-336da68f3478" />

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
<img width="615" height="248" alt="Screenshot 2026-04-30 082127" src="https://github.com/user-attachments/assets/53eb708e-f881-4688-9755-c4746e9963ae" />


# RESULT:
The Commands are executed successfully.
