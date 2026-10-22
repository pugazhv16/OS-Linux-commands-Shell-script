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
<img width="630" height="157" alt="image" src="https://github.com/user-attachments/assets/f520cfa0-1f60-4a0e-a9b9-dabcb1e99f21" />



cat < file2
## OUTPUT
<img width="588" height="177" alt="image" src="https://github.com/user-attachments/assets/818dac18-19e9-4288-be46-fc69f60bb2df" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="592" height="78" alt="image" src="https://github.com/user-attachments/assets/d4af246c-e18e-4035-b3d9-ad965c03cfa2" />

comm file1 file2
 ## OUTPUT
<img width="620" height="233" alt="image" src="https://github.com/user-attachments/assets/484c199c-edb1-487e-af6a-2991b94e345b" />

 
diff file1 file2
## OUTPUT
<img width="595" height="279" alt="image" src="https://github.com/user-attachments/assets/bcbcff62-e9f6-424e-9dc2-f920b142ab44" />


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
<img width="642" height="95" alt="image" src="https://github.com/user-attachments/assets/e4bf44e5-501d-43ce-9b9a-3fe2f496ef6b" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="616" height="134" alt="image" src="https://github.com/user-attachments/assets/7878bfd6-c4c7-497b-8057-231e9e14dade" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="615" height="130" alt="image" src="https://github.com/user-attachments/assets/5a11376d-d8dc-4c4f-8c21-f9b205ed071c" />


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
<img width="578" height="73" alt="image" src="https://github.com/user-attachments/assets/dd0848a9-fcd8-4b59-8bc0-3c4c57174f89" />



grep hello newfile 
## OUTPUT
<img width="571" height="77" alt="image" src="https://github.com/user-attachments/assets/ac7cac41-652e-44c0-9dda-f387ccad5cbd" />




grep -v hello newfile 
## OUTPUT
<img width="576" height="80" alt="image" src="https://github.com/user-attachments/assets/b8c22877-e5cc-4ca2-9df2-fb6f7037ea3c" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="579" height="101" alt="image" src="https://github.com/user-attachments/assets/679b00e1-7900-4a8f-9dbb-05f82e407b0a" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="591" height="82" alt="image" src="https://github.com/user-attachments/assets/de46daef-d119-4439-aad3-f534b07cd2cd" />




grep -R ubuntu /etc
## OUTPUT
<img width="649" height="99" alt="image" src="https://github.com/user-attachments/assets/12517dcc-e2e7-479d-8e23-99375c6dc6a4" />



grep -w -n world newfile   
## OUTPUT
<img width="1277" height="818" alt="image" src="https://github.com/user-attachments/assets/93ccee35-11a8-4e36-b7e7-d0924a63aa4b" />


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

<img width="592" height="99" alt="image" src="https://github.com/user-attachments/assets/c1a546c5-bc7a-4397-97f3-d994c20004ba" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="610" height="94" alt="image" src="https://github.com/user-attachments/assets/e0543b75-b132-45fa-bc86-34a22cc4768f" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="610" height="106" alt="image" src="https://github.com/user-attachments/assets/450f8947-5a2d-454c-b265-6c2a8f3b4c2a" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="608" height="69" alt="image" src="https://github.com/user-attachments/assets/2e112b97-2893-4add-a9bd-4d1327734b95" />



egrep '(world$)' newfile 
## OUTPUT
<img width="572" height="100" alt="image" src="https://github.com/user-attachments/assets/836b090b-e929-424a-a0bd-dfae42b045f6" />



egrep '(World$)' newfile 
## OUTPUT
<img width="605" height="75" alt="image" src="https://github.com/user-attachments/assets/5dfe7cc9-3852-4b65-81d8-19f47055afc9" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="603" height="124" alt="image" src="https://github.com/user-attachments/assets/52e57b4e-0987-42d8-b21d-96ebc64f933b" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="641" height="81" alt="image" src="https://github.com/user-attachments/assets/98e742da-02e7-4686-b7a2-b1a1ecc3ebea" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="627" height="77" alt="image" src="https://github.com/user-attachments/assets/8387967b-0570-427b-ae04-598669838fc8" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="617" height="76" alt="image" src="https://github.com/user-attachments/assets/8a395d09-a5fc-4ea9-a3fc-ecbd3a6924ab" />


egrep l{2} newfile
## OUTPUT

<img width="611" height="102" alt="image" src="https://github.com/user-attachments/assets/08f44a9d-1d7e-4eb1-83a7-7f069b3cd2b2" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="637" height="127" alt="image" src="https://github.com/user-attachments/assets/107057fe-814d-42aa-866e-749a18658649" />


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

<img width="583" height="75" alt="image" src="https://github.com/user-attachments/assets/6ab9e468-7eeb-4e7f-b6fa-784f5c85263b" />


sed -n -e '$p' file23
## OUTPUT

<img width="568" height="70" alt="image" src="https://github.com/user-attachments/assets/4bd1fce4-ad86-4f31-863d-8eecc586a513" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="607" height="247" alt="image" src="https://github.com/user-attachments/assets/200e452c-9a04-42b1-a156-89aaa19bdeea" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="629" height="256" alt="image" src="https://github.com/user-attachments/assets/db106b76-eb43-433b-9c13-78b22237e36c" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="597" height="179" alt="image" src="https://github.com/user-attachments/assets/737bb503-6318-459d-b633-74e9b6843966" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="612" height="126" alt="image" src="https://github.com/user-attachments/assets/a07a8e18-9caa-4429-a23d-b6c32f981bb7" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="612" height="126" alt="image" src="https://github.com/user-attachments/assets/1e9bf06e-84bf-4e8e-b31b-120af134fddf" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="582" height="96" alt="image" src="https://github.com/user-attachments/assets/5a80942b-9ab0-4f1e-aed1-6fafb8fc9c0a" />


seq 10 
## OUTPUT

<img width="575" height="294" alt="image" src="https://github.com/user-attachments/assets/b837f09d-41d3-4882-9eb3-e6a69aca9e82" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="575" height="294" alt="image" src="https://github.com/user-attachments/assets/1fcc9575-8c8a-4b76-9d1a-09faea66a1d6" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="564" height="120" alt="image" src="https://github.com/user-attachments/assets/41016a70-62c8-4def-8cf1-a2416a41505a" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="564" height="120" alt="image" src="https://github.com/user-attachments/assets/9c9cdfa6-7124-497e-bce0-edd43ad1335a" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="591" height="150" alt="image" src="https://github.com/user-attachments/assets/be93da4c-5e2b-4b46-8f2b-e3abbc1e7411" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="569" height="120" alt="image" src="https://github.com/user-attachments/assets/141a2b78-eb77-49ea-a180-ff8486a8700c" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="574" height="121" alt="image" src="https://github.com/user-attachments/assets/9bf89a1c-4db0-4eae-831e-6d28c554bc39" />


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
<img width="332" height="181" alt="image" src="https://github.com/user-attachments/assets/b742310f-03be-4437-906e-18e24ac5ae64" />


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

<img width="346" height="179" alt="image" src="https://github.com/user-attachments/assets/93b29379-bacb-45d6-a75a-4a3dddce3c5a" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="455" height="201" alt="image" src="https://github.com/user-attachments/assets/9f085724-2557-4f2e-b5cd-168da89b3662" />

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
<img width="381" height="125" alt="image" src="https://github.com/user-attachments/assets/92f235d6-d9cc-4dbb-9990-74059a99bd72" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="502" height="126" alt="image" src="https://github.com/user-attachments/assets/3eba82d6-c154-4ad3-871d-6b274815c81c" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="765" height="855" alt="image" src="https://github.com/user-attachments/assets/2d4cf60d-9923-49f2-995b-eb11639babad" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1326" height="871" alt="image" src="https://github.com/user-attachments/assets/5e64103f-15ef-41a7-83c7-bf5236e19740" />


tar -xvf backup.tar
## OUTPUT
<img width="787" height="850" alt="image" src="https://github.com/user-attachments/assets/14ee974a-82f0-4b4d-9d6c-749b1a50f033" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="387" height="71" alt="image" src="https://github.com/user-attachments/assets/ba61218a-a118-48d8-8f03-cc221da7bb0c" />

gunzip backup.tar.gz
## OUTPUT
<img width="1781" height="285" alt="image" src="https://github.com/user-attachments/assets/e6df450e-688b-4809-832b-cad2bc589b5c" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="605" height="79" alt="image" src="https://github.com/user-attachments/assets/3f2820d2-d584-4766-8450-767134c4192d" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="417" height="120" alt="image" src="https://github.com/user-attachments/assets/f9981090-9b0c-4aa5-b1bc-0fbb7d19fb79" />


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
<img width="677" height="391" alt="image" src="https://github.com/user-attachments/assets/31819dbd-1b1e-4e6b-b092-7b2b8bbd6ed5" />

 
ls file1
## OUTPUT
<img width="343" height="75" alt="image" src="https://github.com/user-attachments/assets/2e6c7834-0545-47b8-b82a-00f7cd29e248" />

echo $?
## OUTPUT 
<img width="262" height="84" alt="image" src="https://github.com/user-attachments/assets/49123485-a14e-47b6-b2aa-96490d0ac986" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="523" height="154" alt="image" src="https://github.com/user-attachments/assets/ad95bcc7-7d30-4da7-9713-6600c810c2f5" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="377" height="152" alt="image" src="https://github.com/user-attachments/assets/f05d6941-f4fb-4c85-9b5a-43cc9e9cb309" />


 
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
<img width="622" height="75" alt="image" src="https://github.com/user-attachments/assets/744fff6f-3102-42e3-a921-6b430c9cec77" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="612" height="86" alt="image" src="https://github.com/user-attachments/assets/75fcaadd-b69f-4bea-8618-81e9b0f4d7aa" />


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
<img width="612" height="86" alt="image" src="https://github.com/user-attachments/assets/eec6a463-e380-48bc-a1ca-47e9f7bba104" />

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
<img width="612" height="145" alt="image" src="https://github.com/user-attachments/assets/57d217c8-7663-4cba-b22d-52d850af5c27" />



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
<img width="592" height="108" alt="image" src="https://github.com/user-attachments/assets/454ccbb1-0262-4946-ab9b-98c363e87b76" />

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
<img width="612" height="145" alt="image" src="https://github.com/user-attachments/assets/b047b72f-1d83-4beb-b4bb-d5bab7e486dc" />

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
<img width="597" height="88" alt="image" src="https://github.com/user-attachments/assets/0b6e2e2a-7903-41b1-9a0d-b8c25f518f2a" />


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
<img width="611" height="91" alt="image" src="https://github.com/user-attachments/assets/aa71ead9-f5ed-4690-904e-878333a46fb7" />

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
<img width="437" height="80" alt="image" src="https://github.com/user-attachments/assets/306dc97a-741e-49e0-a20e-473f702af0e6" />

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
<img width="626" height="311" alt="image" src="https://github.com/user-attachments/assets/9f00bf65-a2f8-4e0c-9126-985a87c57196" />


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
<img width="602" height="162" alt="image" src="https://github.com/user-attachments/assets/ca02ff0a-7569-45ca-bde8-f446509bb685" />

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
<img width="655" height="218" alt="image" src="https://github.com/user-attachments/assets/d900d724-ec56-46b1-b2f6-3db2bb0d171c" />

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

 <img width="600" height="140" alt="image" src="https://github.com/user-attachments/assets/8fb18aaf-4d4f-418e-b61f-c9986b5468a4" />

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
<img width="637" height="214" alt="image" src="https://github.com/user-attachments/assets/410700f2-9387-4e6b-9d7b-abb041545827" />

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
<img width="655" height="218" alt="image" src="https://github.com/user-attachments/assets/24d9788a-a2f3-4fe0-a610-dc1f51f99d04" />
 
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

<img width="650" height="223" alt="image" src="https://github.com/user-attachments/assets/4e922c84-d49f-4afc-be2a-3a6036db5037" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="318" height="171" alt="image" src="https://github.com/user-attachments/assets/1279ba91-b1c8-4a33-9e0e-f1de0d079dd8" />



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
<img width="315" height="172" alt="image" src="https://github.com/user-attachments/assets/7884c317-7789-4ac3-9865-aabcc6949bad" />

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
<img width="327" height="131" alt="image" src="https://github.com/user-attachments/assets/d13da181-141c-427c-9f17-695a8939720b" />

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
<img width="321" height="128" alt="image" src="https://github.com/user-attachments/assets/65ad95ab-1f92-4ca7-b5bf-9f01a11b850d" />

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
<img width="321" height="128" alt="image" src="https://github.com/user-attachments/assets/db5940a4-072d-4fba-a991-01b3062fced8" />

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
 <img width="333" height="376" alt="image" src="https://github.com/user-attachments/assets/ce08f197-5556-40d6-8060-40960397ac90" />

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
<img width="386" height="125" alt="image" src="https://github.com/user-attachments/assets/5cdc35db-5772-44a7-85d7-3b98256458b7" />

# RESULT:
The Commands are executed successfully.
