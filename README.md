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

<img width="402" height="124" alt="image" src="https://github.com/user-attachments/assets/5f511eb8-2127-4023-afbf-71f92f854c7f" />


cat < file2
## OUTPUT
<img width="275" height="145" alt="image" src="https://github.com/user-attachments/assets/16052427-6ca4-4e20-a90f-322abde752da" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="332" height="60" alt="image" src="https://github.com/user-attachments/assets/3920a58c-1279-488a-9af8-9046af65cabe" />

comm file1 file2
 ## OUTPUT
<img width="364" height="242" alt="image" src="https://github.com/user-attachments/assets/0ddd2e52-2210-4bf2-8d7e-ae3c0c265c6f" />

 
diff file1 file2
## OUTPUT
<img width="384" height="248" alt="image" src="https://github.com/user-attachments/assets/c625f281-f958-404d-83d1-a6504d43d1a5" />


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
<img width="320" height="122" alt="image" src="https://github.com/user-attachments/assets/49e66f88-074b-425a-8ecd-9fdee60bc573" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="352" height="112" alt="image" src="https://github.com/user-attachments/assets/37c374d2-43b6-408a-9145-1e0c6c0efd9a" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="404" height="102" alt="image" src="https://github.com/user-attachments/assets/67579d62-1e93-43a3-b730-a6a779581a2c" />


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
<img width="363" height="87" alt="image" src="https://github.com/user-attachments/assets/85594ee4-b41d-4bd7-84ea-49650023be3c" />



grep hello newfile 
## OUTPUT
<img width="383" height="90" alt="image" src="https://github.com/user-attachments/assets/21a75979-d950-491e-902f-fe5e5881713d" />




grep -v hello newfile 
## OUTPUT
<img width="348" height="83" alt="image" src="https://github.com/user-attachments/assets/a23174df-9667-456a-9e40-95b4b44ed1c4" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="401" height="77" alt="image" src="https://github.com/user-attachments/assets/404bb42b-8b79-407a-ab5f-282c87239ff3" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="500" height="72" alt="image" src="https://github.com/user-attachments/assets/c13c865f-7f22-4ba7-ac6f-6ce2b547bc84" />





grep -R ubuntu /etc
## OUTPUT
 <img width="534" height="45" alt="image" src="https://github.com/user-attachments/assets/e773075f-56e0-4467-aacd-d6353126559f" />




grep -w -n world newfile   
## OUTPUT
<img width="539" height="193" alt="image" src="https://github.com/user-attachments/assets/38617780-1e9c-46c7-977e-47f1db04d39b" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```
<img width="440" height="69" alt="image" src="https://github.com/user-attachments/assets/cd58ac99-7f60-42b8-b0b4-aa1345984058" />

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

<img width="417" height="87" alt="image" src="https://github.com/user-attachments/assets/e7708a9a-b520-4d0f-bb86-509af4e0a324" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="393" height="84" alt="image" src="https://github.com/user-attachments/assets/457b981d-1444-4455-b180-6d653e17f2a8" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="432" height="85" alt="image" src="https://github.com/user-attachments/assets/56388b19-c014-4c06-b459-2bf5e8face3d" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="443" height="67" alt="image" src="https://github.com/user-attachments/assets/0aca56cd-d541-4013-aaff-db8a0a346188" />



egrep '(world$)' newfile 
## OUTPUT
<img width="369" height="66" alt="image" src="https://github.com/user-attachments/assets/5bb88dad-c218-40d2-8d29-782735b1d47f" />



egrep '(World$)' newfile 
## OUTPUT
<img width="400" height="64" alt="image" src="https://github.com/user-attachments/assets/9663d90e-e8b3-449d-a12b-ec7b70689ffa" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="380" height="69" alt="image" src="https://github.com/user-attachments/assets/2e0a13c8-156d-419c-adf7-f1df07c1ad47" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="408" height="87" alt="image" src="https://github.com/user-attachments/assets/a67160b0-5c34-499a-8478-8e760e08f315" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="400" height="82" alt="image" src="https://github.com/user-attachments/assets/ef77b9ca-cabd-4ba8-a408-f6fc7ea0a747" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="409" height="71" alt="image" src="https://github.com/user-attachments/assets/593ce3de-3336-461c-92d9-cae9644bac2b" />


egrep l{2} newfile
## OUTPUT
<img width="437" height="62" alt="image" src="https://github.com/user-attachments/assets/f4e7f058-29db-4706-a9d8-12ba99a085aa" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="343" height="82" alt="image" src="https://github.com/user-attachments/assets/1754219e-6539-4125-9d07-546e0e76caa9" />

<img width="418" height="97" alt="image" src="https://github.com/user-attachments/assets/f9aa50a5-6de5-4bc2-aca4-c71b4e3a9e81" />

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



sed -n -e '$p' file23
## OUTPUT
<img width="415" height="46" alt="image" src="https://github.com/user-attachments/assets/58cd078c-9571-4679-9058-34494a95024e" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="423" height="52" alt="image" src="https://github.com/user-attachments/assets/f82d4d7f-f1c3-48c0-828d-6d442d8d2445" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="473" height="226" alt="image" src="https://github.com/user-attachments/assets/7a9403e2-17ef-4018-b9dd-48b0cb25a144" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="483" height="208" alt="image" src="https://github.com/user-attachments/assets/a3d3728c-ba19-4e02-b122-7bf7f9df4c06" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="517" height="227" alt="image" src="https://github.com/user-attachments/assets/a1fdee6f-f1ad-4e8b-a3b0-c62b092d88f7" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="442" height="151" alt="image" src="https://github.com/user-attachments/assets/fbfa5722-6d9b-4326-8a6e-7925a488e82f" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="477" height="98" alt="image" src="https://github.com/user-attachments/assets/9773f270-2553-481e-816f-9679bf67d09c" />



seq 10 
## OUTPUT
<img width="508" height="79" alt="image" src="https://github.com/user-attachments/assets/e1cc2357-6736-43c9-9f2b-592d35cf5584" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="305" height="278" alt="image" src="https://github.com/user-attachments/assets/0b36b864-cbdd-45d6-a3b6-6591d4a27796" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="417" height="94" alt="image" src="https://github.com/user-attachments/assets/8d5fe48c-59ac-4ef1-bc07-8f81389a0e09" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="443" height="99" alt="image" src="https://github.com/user-attachments/assets/67a34519-386a-4b53-b84b-4d677f218fdf" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="417" height="121" alt="image" src="https://github.com/user-attachments/assets/a30a2fd2-e789-4de5-aa6c-69ae1f0ef8c7" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="457" height="103" alt="image" src="https://github.com/user-attachments/assets/fc4d455b-e0bf-4950-a0b9-732eaabb9d89" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="503" height="95" alt="image" src="https://github.com/user-attachments/assets/bc65aedf-6fe0-4fee-bc3f-0024209655f4" />



sed -n '2,4{s/$/*/;p}' file23
<img width="505" height="104" alt="image" src="https://github.com/user-attachments/assets/d40d5bc3-78cb-4f58-841f-b4a1bf583025" />


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
<img width="303" height="146" alt="image" src="https://github.com/user-attachments/assets/a9140dda-7710-42ec-8d6e-97fddc3e4d5c" />


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
<img width="322" height="147" alt="image" src="https://github.com/user-attachments/assets/98308586-489e-4e9e-94b5-8444cb64cd11" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="554" height="205" alt="image" src="https://github.com/user-attachments/assets/29ef46e8-7f4c-4850-9084-ccaaf6fae96d" />

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
<img width="472" height="91" alt="image" src="https://github.com/user-attachments/assets/21e00e0c-43ab-4713-8ccc-e333aff2fa41" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="551" height="90" alt="image" src="https://github.com/user-attachments/assets/3f0e6016-7cfb-4766-92a1-0f6799c2776d" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="283" height="129" alt="image" src="https://github.com/user-attachments/assets/ab61320b-f658-4860-b83d-807d46bd58df" />


tar -xvf backup.tar
## OUTPUT
<img width="446" height="152" alt="image" src="https://github.com/user-attachments/assets/9fef37b0-af82-40e0-9d11-cf071317622d" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="561" height="117" alt="image" src="https://github.com/user-attachments/assets/0656976f-2cc1-4fbf-886e-b92a31494a05" />
 
gunzip backup.tar.gz
## OUTPUT

<img width="553" height="176" alt="image" src="https://github.com/user-attachments/assets/46f6ebe1-a848-41c9-9383-31598991a99c" />
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="548" height="232" alt="image" src="https://github.com/user-attachments/assets/c32077ab-2ad8-45f5-becc-2d94923288f2" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="366" height="95" alt="image" src="https://github.com/user-attachments/assets/77a10462-b511-4b8c-9b95-24b1e497fe59" />


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
<img width="430" height="382" alt="image" src="https://github.com/user-attachments/assets/64786f9e-1b69-420a-ab8d-ae61252431b5" />

 
ls file1
## OUTPUT
<img width="249" height="47" alt="image" src="https://github.com/user-attachments/assets/3d3f7a07-2e0c-47cc-a798-86f7c613b96d" />

echo $?
## OUTPUT 
<img width="256" height="46" alt="image" src="https://github.com/user-attachments/assets/7db3dd33-66ed-4ead-ab4d-0ca2362ffbfc" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="244" height="48" alt="image" src="https://github.com/user-attachments/assets/2bff986e-1f49-40eb-8a76-0f664f354784" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="518" height="247" alt="image" src="https://github.com/user-attachments/assets/254ffd75-374a-40c2-9b3f-d79915b22680" />


 
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
<img width="496" height="280" alt="image" src="https://github.com/user-attachments/assets/bbf5900b-2ace-4af9-aeb1-787d772057ee" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="554" height="170" alt="image" src="https://github.com/user-attachments/assets/f64bd64d-34c3-454e-9f3c-c6883f771e76" />


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
<img width="552" height="227" alt="image" src="https://github.com/user-attachments/assets/0f439e98-117f-48d4-9c2a-143596c3789a" />

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
<img width="539" height="521" alt="image" src="https://github.com/user-attachments/assets/aefaeb87-9994-40c2-9d11-870045ac259c" />



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
<img width="534" height="439" alt="image" src="https://github.com/user-attachments/assets/32745aa8-6440-420e-86f2-8688ed2b13a6" />

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
<img width="552" height="535" alt="image" src="https://github.com/user-attachments/assets/e0e0c623-da19-4b0f-817a-2a40212f3d13" />

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
<img width="533" height="433" alt="image" src="https://github.com/user-attachments/assets/f666cb09-5fe1-43bc-be4b-ae92102f6920" />


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
<img width="535" height="541" alt="image" src="https://github.com/user-attachments/assets/aea72a5e-4905-4dae-9727-8068cdf2ba4d" />

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
<img width="407" height="225" alt="image" src="https://github.com/user-attachments/assets/dcd83bdf-47ff-4aab-9d78-f5ea1c252efe" />


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
<img width="418" height="231" alt="image" src="https://github.com/user-attachments/assets/255fc3b2-83d7-4e79-a1e9-4bd2da315de5" />

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
<img width="416" height="222" alt="image" src="https://github.com/user-attachments/assets/ed7ececc-c583-43ee-ab1d-fc380badd07a" />

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
<img width="554" height="219" alt="image" src="https://github.com/user-attachments/assets/38011959-35b7-402e-9ac8-2604abcedc59" />

 
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
<img width="560" height="219" alt="image" src="https://github.com/user-attachments/assets/87e6dc8e-6327-4343-b0cb-1b00cb63e67d" />

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
<img width="454" height="267" alt="image" src="https://github.com/user-attachments/assets/1e4fd3ea-ffd1-4168-b81c-27e44c7a3b1f" />
 
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
<img width="435" height="123" alt="image" src="https://github.com/user-attachments/assets/b4f883d1-5dab-4875-a777-6bf7db3162bd" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="488" height="159" alt="image" src="https://github.com/user-attachments/assets/2fbad59a-846e-48a1-8f73-d4091954a1af" />



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
 ./funcex.sh <img width="318" height="29" alt="image" src="https://github.com/user-attachments/assets/360ca394-29a2-4999-b470-9be1424e338d" />


 
 ./funcex.sh 1 2
<img width="281" height="28" alt="image" src="https://github.com/user-attachments/assets/78528e84-e7c0-4d1b-a35b-e50280b1d78a" />

 
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
<img width="129" height="54" alt="image" src="https://github.com/user-attachments/assets/b85d2897-4221-425e-bc88-910495049dfb" />

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
<img width="130" height="79" alt="image" src="https://github.com/user-attachments/assets/bcba5315-3515-44e6-9981-871dfd2f4786" />

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
<img width="281" height="319" alt="image" src="https://github.com/user-attachments/assets/4944e3bc-a302-47b3-a251-44c4298a9884" />

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
 <img width="301" height="46" alt="image" src="https://github.com/user-attachments/assets/3216c2d7-fa15-4025-b081-08ccdf2250bf" />

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
<img width="238" height="215" alt="image" src="https://github.com/user-attachments/assets/6842c267-d45e-4663-bdcc-4fa82afcb469" />


# RESULT:
The Commands are executed successfully.
