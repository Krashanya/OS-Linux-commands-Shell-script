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

<img width="575" height="228" alt="image" src="https://github.com/user-attachments/assets/86d998d8-6a75-4f1c-b51a-6fd312b89e02" />


cat < file2
## OUTPUT

<img width="569" height="203" alt="image" src="https://github.com/user-attachments/assets/fb242971-0458-4291-a822-ff65dd1f57d8" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="627" height="138" alt="image" src="https://github.com/user-attachments/assets/349372b3-3673-417f-94b2-15e5fc2631f6" />

comm file1 file2
 ## OUTPUT
<img width="793" height="208" alt="image" src="https://github.com/user-attachments/assets/f2cae303-e755-485c-912b-bc498cb0b518" />

diff file1 file2
## OUTPUT
<img width="795" height="367" alt="image" src="https://github.com/user-attachments/assets/03e3c061-71b0-4f6b-bd15-dfc590e2c958" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
<img width="747" height="106" alt="image" src="https://github.com/user-attachments/assets/6b6f81ef-cdd6-455a-b9e6-17e5679acfd9" />

cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
<img width="714" height="125" alt="image" src="https://github.com/user-attachments/assets/5aa6eb33-8218-421b-b168-4c94aefb1a52" />

cut -c1-3 file11
## OUTPUT
<img width="739" height="104" alt="image" src="https://github.com/user-attachments/assets/82d2f1a3-e7af-4f80-9485-23b5f5550cc9" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="721" height="126" alt="image" src="https://github.com/user-attachments/assets/41b83c69-4b0a-4454-814e-13bd0b79516e" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="702" height="129" alt="image" src="https://github.com/user-attachments/assets/3619f71c-c813-484d-8fc7-35f8d9c8c088" />

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

<img width="662" height="108" alt="image" src="https://github.com/user-attachments/assets/d5cbcdf8-4c57-400f-bf15-f771b74abd83" />


grep hello newfile 
## OUTPUT

<img width="653" height="80" alt="image" src="https://github.com/user-attachments/assets/c17a3959-93f4-4930-84cf-8ca67395ac6f" />



grep -v hello newfile 
## OUTPUT

<img width="718" height="76" alt="image" src="https://github.com/user-attachments/assets/fa527a72-590a-4afa-82d5-7c177359c6ed" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="597" height="107" alt="image" src="https://github.com/user-attachments/assets/28a6950d-c2a7-4b06-940a-303c850cc19e" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="658" height="82" alt="image" src="https://github.com/user-attachments/assets/d1c99ec6-7500-482c-842f-29836ad1a2d5" />


grep -R ubuntu /etc
## OUTPUT
<img width="1138" height="512" alt="image" src="https://github.com/user-attachments/assets/3ffabf2d-2fcc-44eb-9db1-a6f7521a1735" />



grep -w -n world newfile   
## OUTPUT
<img width="678" height="102" alt="image" src="https://github.com/user-attachments/assets/57c1a328-0c08-4e95-bbb8-dd06906a0d7d" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```
<img width="629" height="179" alt="image" src="https://github.com/user-attachments/assets/d3a67c1b-0e98-4dce-8a2a-59274cbec527" />

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
<img width="645" height="105" alt="image" src="https://github.com/user-attachments/assets/0b2d0e12-dd00-4259-90fd-07e9eb2e2861" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="603" height="101" alt="image" src="https://github.com/user-attachments/assets/0e81d8c2-94bb-451e-8910-7c314afb0fd3" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="592" height="103" alt="image" src="https://github.com/user-attachments/assets/47d5259c-cc27-4540-bfe2-cb01cd162ef5" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="574" height="79" alt="image" src="https://github.com/user-attachments/assets/7969f227-8b07-436f-9262-796e0ac2cd68" />


egrep '(world$)' newfile 
## OUTPUT
<img width="571" height="121" alt="image" src="https://github.com/user-attachments/assets/b8a449db-c81f-4942-9790-241343a1238a" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="783" height="132" alt="image" src="https://github.com/user-attachments/assets/880af5f2-7225-483c-8f5c-0e378a1ecf93" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="635" height="81" alt="image" src="https://github.com/user-attachments/assets/55819fb8-8c0d-4456-9cae-d8c4935a889a" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="616" height="107" alt="image" src="https://github.com/user-attachments/assets/a5ac9526-deb4-4506-a4d1-9d2b4f655324" />


egrep l{2} newfile
## OUTPUT
<img width="625" height="105" alt="image" src="https://github.com/user-attachments/assets/4d8dea43-796f-4da4-87f9-528ddae4aaee" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="615" height="128" alt="image" src="https://github.com/user-attachments/assets/30ea00ce-db7e-4f3b-a931-bbb9231ec758" />


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
<img width="636" height="260" alt="image" src="https://github.com/user-attachments/assets/b8d17671-2367-4433-8ddf-83942f410d77" />


sed -n -e '3p' file23
## OUTPUT

<img width="592" height="83" alt="image" src="https://github.com/user-attachments/assets/e6ccef04-ba60-4e3a-ac44-89520c2b4df8" />


sed -n -e '$p' file23
## OUTPUT

<img width="574" height="72" alt="image" src="https://github.com/user-attachments/assets/cac82104-5c58-4edf-b36a-8c7797f989b1" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="588" height="255" alt="image" src="https://github.com/user-attachments/assets/46f8d3e6-7f32-4a97-a828-cf0a91c2e590" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="579" height="253" alt="image" src="https://github.com/user-attachments/assets/200c8df2-6fc6-4c35-9f9e-5037ef3bb7bf" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="681" height="255" alt="image" src="https://github.com/user-attachments/assets/62cf979a-6c8a-423b-a31a-cfb9bda7a232" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="605" height="172" alt="image" src="https://github.com/user-attachments/assets/b0b0c5ff-722e-4b43-b771-93bc38af5aea" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="625" height="203" alt="image" src="https://github.com/user-attachments/assets/b7433d0e-427f-4552-9f35-40a5a02863d3" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="576" height="182" alt="image" src="https://github.com/user-attachments/assets/ab4ca643-c943-4095-8b19-e6334022f95e" />


seq 10 
## OUTPUT
<img width="618" height="304" alt="image" src="https://github.com/user-attachments/assets/af7c6f00-1ca0-4ee6-add1-a3c07564b1a0" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="581" height="118" alt="image" src="https://github.com/user-attachments/assets/6033f15a-388c-45f5-bbcd-aec1801cfbe3" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="637" height="123" alt="image" src="https://github.com/user-attachments/assets/823c26a4-b8fb-4bb7-b703-d166b3a90b2f" />

seq 3 | sed '2a hello'
## OUTPUT

<img width="599" height="159" alt="image" src="https://github.com/user-attachments/assets/56565a75-536f-459c-acd6-f2b560cee430" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="624" height="140" alt="image" src="https://github.com/user-attachments/assets/348f0758-8a7c-4548-a486-dab912e37669" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="622" height="122" alt="image" src="https://github.com/user-attachments/assets/39edfb63-d632-4a72-9d96-5744fcf292b8" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="585" height="133" alt="image" src="https://github.com/user-attachments/assets/b8c76d7b-d74e-4f72-8d3b-a598275dcc2a" />

sed -n '2,4{s/$/*/;p}' file23

<img width="584" height="126" alt="image" src="https://github.com/user-attachments/assets/1c0b7aca-53cb-42db-b605-80e496998463" />

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
<img width="694" height="183" alt="image" src="https://github.com/user-attachments/assets/589e33b1-a2cf-4355-bfad-41a51d1d712d" />


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

<img width="560" height="173" alt="image" src="https://github.com/user-attachments/assets/1d3b1c01-383e-4591-8929-e2c1c238f0b6" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="623" height="249" alt="image" src="https://github.com/user-attachments/assets/1c6f442c-85d7-46f6-b4f1-46e71a252a3b" />

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

<img width="577" height="128" alt="image" src="https://github.com/user-attachments/assets/87b8b6a0-04de-4f1e-ab7b-eae47704dfd5" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="604" height="123" alt="image" src="https://github.com/user-attachments/assets/2459d28f-7c79-4fa6-8811-fd501e10d8d1" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="662" height="249" alt="image" src="https://github.com/user-attachments/assets/eeeb651c-9359-4a8a-903f-5e70b1833ce4" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="744" height="405" alt="image" src="https://github.com/user-attachments/assets/2798ce74-0311-49b6-ae6e-bea1e59388fe" />


tar -xvf backup.tar
## OUTPUT
<img width="691" height="241" alt="image" src="https://github.com/user-attachments/assets/d3476527-fded-427f-853f-421ca28de92b" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="562" height="231" alt="image" src="https://github.com/user-attachments/assets/dbcc4402-e1f8-4a4a-9248-bbade29e5f43" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="409" height="278" alt="image" src="https://github.com/user-attachments/assets/f5af3509-9294-4036-b3d1-db385e034271" />

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
<img width="696" height="303" alt="image" src="https://github.com/user-attachments/assets/10360f64-7c4d-4b16-8649-c52c7de91fdc" />

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

 <img width="709" height="509" alt="image" src="https://github.com/user-attachments/assets/f8ded7b2-f0a0-4304-98e6-5eddc95e0e2b" />

ls file1
## OUTPUT
<img width="378" height="81" alt="image" src="https://github.com/user-attachments/assets/3f547c63-af78-4b36-bf16-6ca06e1820b3" />

echo $?
## OUTPUT 
<img width="274" height="72" alt="image" src="https://github.com/user-attachments/assets/c92c015e-1632-4954-8ba1-ec520fb52153" />


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

<img width="448" height="270" alt="image" src="https://github.com/user-attachments/assets/cf36dd70-20d3-436b-9555-c79da87adfb4" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="645" height="154" alt="image" src="https://github.com/user-attachments/assets/eaf93336-b076-42bb-9126-2e99ed4e9535" />


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
<img width="728" height="231" alt="image" src="https://github.com/user-attachments/assets/1b67ece8-8ef5-4990-b025-13578ff7f3b6" />

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
<img width="455" height="83" alt="image" src="https://github.com/user-attachments/assets/2bdf3911-73bb-4cdb-a7db-e683769bd4e4" />

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
<img width="546" height="472" alt="image" src="https://github.com/user-attachments/assets/b14b1bea-4f69-4a2b-bcce-2aa4c2c3a939" />

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

<img width="535" height="85" alt="image" src="https://github.com/user-attachments/assets/55379f46-d163-40fc-b291-667fdda079d4" />


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
<img width="528" height="376" alt="image" src="https://github.com/user-attachments/assets/a516e1b4-3b2c-4e00-90d9-428b83bf179e" />


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
<img width="688" height="253" alt="image" src="https://github.com/user-attachments/assets/1172bc04-d23c-459d-9a5d-f830ee32ae72" />

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
<img width="658" height="178" alt="image" src="https://github.com/user-attachments/assets/7e91684b-fc03-4d91-8afe-90a28d2e3d62" />

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
<img width="709" height="515" alt="image" src="https://github.com/user-attachments/assets/fe72aea4-f4e1-4e7f-9aec-963063f2e6d3" />

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
<img width="736" height="152" alt="image" src="https://github.com/user-attachments/assets/78ab75ea-949a-4bab-84ec-de19229d90cd" />


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
<img width="499" height="231" alt="image" src="https://github.com/user-attachments/assets/1d1b255f-67d1-409e-a747-1482e858a33a" />

$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="644" height="155" alt="image" src="https://github.com/user-attachments/assets/99c626d7-5f23-4d26-956f-44415338b539" />

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
<img width="643" height="320" alt="image" src="https://github.com/user-attachments/assets/b2db5123-0100-4a2a-9738-db44a574fca6" />

$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
OUTPUT:
<img width="368" height="133" alt="image" src="https://github.com/user-attachments/assets/fd753635-7ed3-4c6c-9f98-5ba1fd3ae0e7" />

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
<img width="395" height="232" alt="image" src="https://github.com/user-attachments/assets/e7b008a0-f58e-4041-8359-991109af31bc" />

$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
OUTPUT:

 <img width="690" height="426" alt="image" src="https://github.com/user-attachments/assets/300ed66c-a781-4a58-937f-382ecce75860" />

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
<img width="653" height="261" alt="image" src="https://github.com/user-attachments/assets/eb813c96-12b9-4051-b819-bfb7f48b3ee4" />

$ chmod 755 untiltest.sh
 OUTPUT:
 <img width="650" height="250" alt="image" src="https://github.com/user-attachments/assets/b911f4d1-703b-4abc-9840-a04b5d4acd81" />

 
 
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
## OUTPUT
<img width="658" height="503" alt="image" src="https://github.com/user-attachments/assets/57e2aa5c-001f-498b-acd7-0a45b0b14886" />

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
## OUTPUT
<img width="683" height="381" alt="image" src="https://github.com/user-attachments/assets/1258f33f-a3bb-402a-8398-c150a7021e30" />

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
<img width="767" height="529" alt="image" src="https://github.com/user-attachments/assets/4f634914-ba4f-4589-973b-9e460bfdd850" />

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
 <img width="749" height="428" alt="image" src="https://github.com/user-attachments/assets/ca278ca4-b3d5-4ef4-9f8e-f94238dbec53" />

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
<img width="666" height="351" alt="image" src="https://github.com/user-attachments/assets/53f20fe8-5f5f-4648-a06a-d9df642de663" />

 
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
<img width="628" height="454" alt="image" src="https://github.com/user-attachments/assets/2c1f5589-cf08-47c7-96b0-bb26f05d2922" />

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
<img width="715" height="298" alt="image" src="https://github.com/user-attachments/assets/baed056b-e802-4797-a2b4-d4beb4fda0f8" />

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
<img width="613" height="350" alt="image" src="https://github.com/user-attachments/assets/f0b5b36b-1602-4cac-a0c0-2e78370b9783" />

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
