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
<img width="377" height="251" alt="image" src="https://github.com/user-attachments/assets/4f7995d0-0236-481f-9dbb-3437d7c5c771" />



cat < file2
## OUTPUT
<img width="382" height="251" alt="image" src="https://github.com/user-attachments/assets/8d889d52-22e6-4d84-a191-b53dea03369b" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="565" height="107" alt="image" src="https://github.com/user-attachments/assets/d8eaaabe-99d5-480a-9894-b4c2c55c0547" />

comm file1 file2
 ## OUTPUT

 <img width="506" height="412" alt="image" src="https://github.com/user-attachments/assets/9fd27278-a745-420f-8836-2265ea9adaad" />

diff file1 file2
## OUTPUT
<img width="495" height="481" alt="image" src="https://github.com/user-attachments/assets/fdb285e9-fbf9-48c7-bab7-1cee76db87f4" />


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
<img width="492" height="222" alt="image" src="https://github.com/user-attachments/assets/bf925f13-6298-4952-96e2-a570bbf346fb" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="585" height="212" alt="image" src="https://github.com/user-attachments/assets/273f64d5-dad8-4159-879d-ec8379b36535" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="588" height="215" alt="image" src="https://github.com/user-attachments/assets/65e411ae-3f15-4a33-ba16-df7b030c6f71" />


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
<img width="526" height="123" alt="image" src="https://github.com/user-attachments/assets/325914f5-aa3b-4168-8f9e-9b9a2bd0340f" />



grep hello newfile 
## OUTPUT

<img width="518" height="106" alt="image" src="https://github.com/user-attachments/assets/508f9331-dccf-4b14-95ab-de0b66428165" />



grep -v hello newfile 
## OUTPUT
<img width="568" height="152" alt="image" src="https://github.com/user-attachments/assets/d2c9d924-8e78-4f41-9701-a956dbdc634f" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="683" height="135" alt="image" src="https://github.com/user-attachments/assets/f417b539-1ad3-475e-bad9-b1e96fc40d9d" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="670" height="100" alt="image" src="https://github.com/user-attachments/assets/73b80652-e0db-4ec8-b0bb-eca51c180924" />



grep -w -n world newfile   
## OUTPUT

<img width="622" height="147" alt="image" src="https://github.com/user-attachments/assets/924057e5-511e-4501-aacf-ba283e08f62d" />

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
<img width="688" height="142" alt="image" src="https://github.com/user-attachments/assets/e4e04581-bb17-4832-bc35-04cffb40c217" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="681" height="131" alt="image" src="https://github.com/user-attachments/assets/1ddcfcd2-597e-46cb-9973-84250b94e47f" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="663" height="126" alt="image" src="https://github.com/user-attachments/assets/73f63460-05eb-4e20-a5fe-17b4f647b64c" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="631" height="115" alt="image" src="https://github.com/user-attachments/assets/cdaebbfa-481f-4176-bfab-68d01824a044" />



egrep '(world$)' newfile 
## OUTPUT
<img width="623" height="135" alt="image" src="https://github.com/user-attachments/assets/2de0686e-1975-4d1b-961e-73d8f61a0d85" />



egrep '(World$)' newfile 
## OUTPUT
<img width="606" height="102" alt="image" src="https://github.com/user-attachments/assets/54013039-1c4f-406f-ae19-2a68c21ca24d" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="697" height="180" alt="image" src="https://github.com/user-attachments/assets/a298e576-d9bb-42d8-b599-0d0414d5aa82" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="558" height="100" alt="image" src="https://github.com/user-attachments/assets/42130578-809b-4003-b9e5-99fa21696c0e" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="677" height="107" alt="image" src="https://github.com/user-attachments/assets/0df2a8a7-8d9a-4221-951b-af5f1eab9e25" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="670" height="107" alt="image" src="https://github.com/user-attachments/assets/53c825b1-ba35-4940-a6ec-f0afb9d2919b" />


egrep l{2} newfile
## OUTPUT
<img width="537" height="147" alt="image" src="https://github.com/user-attachments/assets/128b1a21-e950-4b3d-9ff7-14b134aac379" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="596" height="177" alt="image" src="https://github.com/user-attachments/assets/3df60db9-d25e-481b-b5b2-754991535a75" />


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
<img width="570" height="106" alt="image" src="https://github.com/user-attachments/assets/f13a85ed-d627-4983-b9e2-c4e3acb3a87a" />



sed -n -e '$p' file23
## OUTPUT
<img width="592" height="127" alt="image" src="https://github.com/user-attachments/assets/4dfb1aae-9480-43cd-bc6a-6e441f3fb5cb" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="652" height="366" alt="image" src="https://github.com/user-attachments/assets/836effc7-d591-4b72-827e-da966ed6bc31" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="687" height="372" alt="image" src="https://github.com/user-attachments/assets/e0cad1cb-c27e-4eb4-b5b3-da5bbdb3956f" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="673" height="362" alt="image" src="https://github.com/user-attachments/assets/903d9235-4bc5-4ffa-9f69-83a8b26a7cad" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="610" height="257" alt="image" src="https://github.com/user-attachments/assets/74189af4-878a-437b-b647-85b838c2d125" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="671" height="182" alt="image" src="https://github.com/user-attachments/assets/b91a3252-e9c6-432c-9cbe-5479d7b19090" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="681" height="122" alt="image" src="https://github.com/user-attachments/assets/e7f7ac78-928e-4ace-bded-a388b73b1295" />



seq 10 
## OUTPUT
<img width="433" height="420" alt="image" src="https://github.com/user-attachments/assets/c7f2b82e-9406-432d-b420-41102bbbba81" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="575" height="173" alt="image" src="https://github.com/user-attachments/assets/28532172-bbe8-4435-ba32-608b26baaf28" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="596" height="177" alt="image" src="https://github.com/user-attachments/assets/e5a89415-4b62-4f27-9e5e-cc0ed1f79acc" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="598" height="210" alt="image" src="https://github.com/user-attachments/assets/7a23f922-ec01-497c-b517-19f03eb1a7dc" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="597" height="181" alt="image" src="https://github.com/user-attachments/assets/ea1950f0-25d8-4473-ba8a-0e79b6da1959" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="631" height="180" alt="image" src="https://github.com/user-attachments/assets/43bfb1d9-e3f6-4be4-a9b9-2231589cf7e7" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="687" height="167" alt="image" src="https://github.com/user-attachments/assets/7b10f867-9fac-4113-b6d4-33eb9c935660" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="677" height="161" alt="image" src="https://github.com/user-attachments/assets/14d2c56a-c5cc-4d08-876c-743217b6d7e3" />


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
<img width="507" height="280" alt="image" src="https://github.com/user-attachments/assets/2eb0b883-e3c5-45f0-b6a7-af347df688da" />


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
<img width="570" height="238" alt="image" src="https://github.com/user-attachments/assets/62c555b2-3bda-424f-bf18-b87579e57cb6" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="667" height="313" alt="image" src="https://github.com/user-attachments/assets/1c495300-1561-4a97-8efb-77c9cad6d4ae" />

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
<img width="667" height="220" alt="image" src="https://github.com/user-attachments/assets/de9c8131-a3ba-4d9d-a141-342e751b262f" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="690" height="182" alt="image" src="https://github.com/user-attachments/assets/3e9a5c21-b698-4ae6-a190-73c8034f4117" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="576" height="396" alt="image" src="https://github.com/user-attachments/assets/41f8ce38-472e-4c20-8d44-de5ef53d7b74" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="712" height="332" alt="image" src="https://github.com/user-attachments/assets/d7070683-5e0d-45ed-967c-d037449ae534" />


tar -xvf backup.tar
## OUTPUT
<img width="697" height="390" alt="image" src="https://github.com/user-attachments/assets/6a13c84c-8970-423e-b9c1-069389fe2c6d" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
<img width="696" height="331" alt="image" src="https://github.com/user-attachments/assets/6f35a8a6-e380-4bc2-bf6b-21e321b0bc03" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="692" height="387" alt="image" src="https://github.com/user-attachments/assets/54b663b8-f725-4c3a-adfa-83e52cc10565" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="501" height="190" alt="image" src="https://github.com/user-attachments/assets/3bd249b3-e278-4910-8de1-c9dcaa954051" />


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
<img width="377" height="662" alt="image" src="https://github.com/user-attachments/assets/c3ef6a89-8a0a-41f3-bfa1-7b8cd14db1bd" />
<img width="472" height="291" alt="image" src="https://github.com/user-attachments/assets/33339c80-b5f8-4a68-8ab4-41951c78ecb5" />

 
ls file1
## OUTPUT
<img width="255" height="71" alt="image" src="https://github.com/user-attachments/assets/18bd9e46-75e8-4362-817a-dd0c860b9007" />

echo $?
## OUTPUT 
<img width="266" height="90" alt="image" src="https://github.com/user-attachments/assets/a2434990-d65c-41a6-ba83-1764c8040592" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="271" height="87" alt="image" src="https://github.com/user-attachments/assets/edff8c2a-b40f-4fe1-bc74-ff9261d01470" />

abcd echo $?
 ## OUTPUT

<img width="332" height="95" alt="image" src="https://github.com/user-attachments/assets/e87ed262-c311-4e6a-a37f-2f348dc86c96" />

 
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
## OUTPUT
<img width="455" height="223" alt="image" src="https://github.com/user-attachments/assets/0d84c75c-ff7c-42ae-94f5-868c9826601d" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="400" height="127" alt="image" src="https://github.com/user-attachments/assets/bd0fbd6f-85e6-47d2-b89e-321f9f41b429" />


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
<img width="437" height="86" alt="image" src="https://github.com/user-attachments/assets/c47c97cd-282c-48fa-aaa0-77e277ff50c9" />

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
<img width="495" height="100" alt="image" src="https://github.com/user-attachments/assets/645c7dca-9574-4017-8af0-0bacb216bc8e" />



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
<img width="447" height="126" alt="image" src="https://github.com/user-attachments/assets/92079ad6-7580-426f-b380-6d191e9afa1d" />

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
<img width="470" height="133" alt="image" src="https://github.com/user-attachments/assets/7beaa932-7e9a-40dd-920b-17a292928896" />

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
<img width="465" height="208" alt="image" src="https://github.com/user-attachments/assets/93a7e983-35b6-4350-8338-27a33ff592eb" />


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
<img width="488" height="116" alt="image" src="https://github.com/user-attachments/assets/22e6a2a1-5696-4703-9cd1-c3f96759d1bc" />

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
## OUTPUT
<img width="505" height="206" alt="image" src="https://github.com/user-attachments/assets/074a63cb-92b1-40cb-9896-4f87ff7decc9" />

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
 <img width="430" height="337" alt="image" src="https://github.com/user-attachments/assets/1b31b55f-9cd3-4cc2-97e9-7e25b1966428" />

 
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
## OUTPUT
 <img width="485" height="182" alt="image" src="https://github.com/user-attachments/assets/2738bbf4-424d-481d-852e-887451ccd050" />

 
 
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
 <img width="446" height="235" alt="image" src="https://github.com/user-attachments/assets/b3f4d232-4b8b-43dd-a09d-9936337fe102" />

 
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
 ## OUTPUT
 <img width="427" height="157" alt="image" src="https://github.com/user-attachments/assets/8497ce2c-2330-46e7-995d-894308ef413b" />

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
 ## OUTPUT
 <img width="420" height="175" alt="image" src="https://github.com/user-attachments/assets/57567074-bf3f-440d-8acc-fe8cb25412e0" />

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
  ## OUTPUT
  <img width="430" height="242" alt="image" src="https://github.com/user-attachments/assets/7438c0d5-d42c-43bc-96c5-994049552aae" />

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
<img width="427" height="230" alt="image" src="https://github.com/user-attachments/assets/ae9faa93-2be8-4fd1-b717-96e9fd327274" />

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
<img width="343" height="77" alt="image" src="https://github.com/user-attachments/assets/59f9858a-f1f2-4b2b-ab26-16975b5d8844" />


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
<img width="416" height="227" alt="image" src="https://github.com/user-attachments/assets/cd4cc4c0-2d42-4f3b-98a4-749e5cc8c9e1" />

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
<img width="421" height="218" alt="image" src="https://github.com/user-attachments/assets/511f1623-a3b5-4098-a39f-d552296d09dd" />

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

 <img width="527" height="385" alt="image" src="https://github.com/user-attachments/assets/66a34a5f-16e6-4f8f-9774-88d13d8ad168" />

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
<img width="422" height="153" alt="image" src="https://github.com/user-attachments/assets/b8b0235e-b685-43f7-8794-5e1043bf04a1" />

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
 <img width="451" height="202" alt="image" src="https://github.com/user-attachments/assets/20b72b4f-0f7c-47d2-92e9-d8519079aec1" />

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
<img width="467" height="137" alt="image" src="https://github.com/user-attachments/assets/6e4ef4b2-fd10-4335-9929-ea18b1a1a8e8" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="438" height="140" alt="image" src="https://github.com/user-attachments/assets/ce8515eb-75a4-4557-bcd2-afb3990a70f8" />



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
<img width="420" height="105" alt="image" src="https://github.com/user-attachments/assets/89310f72-1d1c-4155-b49d-37a8ff805dc2" />

 
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
 <img width="441" height="167" alt="image" src="https://github.com/user-attachments/assets/32ed932c-7980-4a44-94a3-012597cc7cee" />

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
 <img width="463" height="157" alt="image" src="https://github.com/user-attachments/assets/926f4cea-501c-4fe0-a392-3abb080bce43" />

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
 <img width="453" height="407" alt="image" src="https://github.com/user-attachments/assets/5a9de2e2-d9a3-46cd-813b-405febc24724" />

 
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
 <img width="437" height="73" alt="image" src="https://github.com/user-attachments/assets/b2185a84-002a-431e-91ea-18913d5765a8" />

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
<img width="440" height="151" alt="image" src="https://github.com/user-attachments/assets/99696337-0259-42fb-bad7-097c470abc95" />


# RESULT:
The Commands are executed successfully.
