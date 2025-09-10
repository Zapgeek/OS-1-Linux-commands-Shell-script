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
<img width="512" height="99" alt="Screenshot from 2025-08-12 11-21-44" src="https://github.com/user-attachments/assets/17b1b04e-1fea-4f7b-a7bb-0abe6111b715" />



cat < file2
## OUTPUT
<img width="519" height="117" alt="Screenshot from 2025-08-12 11-21-59" src="https://github.com/user-attachments/assets/97c9ac12-e787-4716-8fdc-2fd7ee0e063b" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="551" height="44" alt="Screenshot from 2025-08-12 11-22-21" src="https://github.com/user-attachments/assets/7c606a81-daf4-4b47-9bd8-c2a328f448f8" />

comm file1 file2
 ## OUTPUT
<img width="556" height="152" alt="Screenshot from 2025-08-12 11-22-47" src="https://github.com/user-attachments/assets/24e4335b-427f-4bc5-9578-ff5e5f9b3ba1" />

 
diff file1 file2
## OUTPUT
<img width="562" height="190" alt="Screenshot from 2025-08-12 11-23-07" src="https://github.com/user-attachments/assets/dc1d2101-2e52-4b52-a31b-c65e24f78673" />


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
<img width="557" height="65" alt="image" src="https://github.com/user-attachments/assets/b595b885-8a5a-4d89-946e-891f3669393f" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="616" height="77" alt="image" src="https://github.com/user-attachments/assets/f0d6d440-067d-4c3d-9192-e45ff82a4780" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="616" height="77" alt="image" src="https://github.com/user-attachments/assets/e3d0547c-69f7-4704-aa1d-5ade70b82c53" />


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

<img width="600" height="43" alt="image" src="https://github.com/user-attachments/assets/20ac9f94-7e8e-48d9-aedc-772692e2c8a0" />



grep hello newfile 
## OUTPUT

<img width="600" height="43" alt="image" src="https://github.com/user-attachments/assets/f9875182-46c4-4640-9d6a-130a2d96721c" />



grep -v hello newfile 
## OUTPUT

<img width="600" height="43" alt="image" src="https://github.com/user-attachments/assets/aeb518ba-5eee-472c-bd85-7f02e0e78228" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="680" height="58" alt="image" src="https://github.com/user-attachments/assets/ec919056-3cee-4eda-807a-b57b1ffc563d" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="708" height="41" alt="image" src="https://github.com/user-attachments/assets/8dd54d94-5d97-4b3e-86d1-b15ae2b2ce7f" />



grep -R ubuntu /etc
## OUTPUT

<img width="730" height="429" alt="image" src="https://github.com/user-attachments/assets/2452b0bf-e881-4df3-b1e5-eb6ccd49b89a" />


grep -w -n world newfile   
## OUTPUT

<img width="710" height="62" alt="image" src="https://github.com/user-attachments/assets/985bd90b-33e3-44ae-9d06-060cd5bb36ce" />


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
<img width="707" height="41" alt="image" src="https://github.com/user-attachments/assets/dedd2c68-579f-40c8-aa2f-8521dece6974" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
  
 <img width="715" height="56" alt="image" src="https://github.com/user-attachments/assets/bf936e26-3a38-4e0f-a10f-49658fd2dbaa" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="711" height="49" alt="image" src="https://github.com/user-attachments/assets/59b6c3df-98f5-4364-aa28-ba0184cccedb" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="715" height="44" alt="image" src="https://github.com/user-attachments/assets/8aa52339-6463-4ee4-bd3a-671d139c9c85" />

 

egrep '(world$)' newfile 
## OUTPUT

<img width="710" height="19" alt="image" src="https://github.com/user-attachments/assets/8c35c8af-18df-4418-9fea-e4466d474c1e" />


egrep '(World$)' newfile 
## OUTPUT

<img width="710" height="64" alt="image" src="https://github.com/user-attachments/assets/6fcddae9-e54e-40b1-bdd5-c3a6e15bbda2" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
 <img width="710" height="64" alt="image" src="https://github.com/user-attachments/assets/6b8c2ab9-118d-47ed-a737-ccc3c42b49c7" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="705" height="45" alt="image" src="https://github.com/user-attachments/assets/8f7ea281-c9cd-4362-a809-79ea87c11b9c" />


egrep 'Linux.*world' newfile 
## OUTPUT
 <img width="708" height="38" alt="image" src="https://github.com/user-attachments/assets/8e398115-68c2-423a-843e-c04bc577ff1a" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="708" height="38" alt="image" src="https://github.com/user-attachments/assets/8e398115-68c2-423a-843e-c04bc577ff1a" />

egrep l{2} newfile
## OUTPUT

<img width="704" height="60" alt="image" src="https://github.com/user-attachments/assets/d5f3b2bb-ab40-4287-bba7-96d0ebcaa26d" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="708" height="38" alt="image" src="https://github.com/user-attachments/assets/17c75e3a-8013-4800-8219-8813549e3e05" />


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

<img width="708" height="38" alt="image" src="https://github.com/user-attachments/assets/f236d7ed-45c0-4833-b74d-a9c3b3d15aae" />


sed -n -e '$p' file23
## OUTPUT
<img width="708" height="38" alt="image" src="https://github.com/user-attachments/assets/3a104bda-f868-4ed3-9c35-9d0276bc7869" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="702" height="164" alt="image" src="https://github.com/user-attachments/assets/5e39a4fe-4354-41ba-b31b-84ed2ee35be4" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="661" height="170" alt="image" src="https://github.com/user-attachments/assets/a5196825-8412-483e-9f0d-b48daae0b558" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="695" height="172" alt="image" src="https://github.com/user-attachments/assets/3c4a9a66-74a8-4e24-8941-bc68482f7271" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="676" height="113" alt="image" src="https://github.com/user-attachments/assets/d8be2ab5-f1da-4fd6-9339-232fed675eea" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="681" height="80" alt="image" src="https://github.com/user-attachments/assets/3ff1945b-6777-48ca-95fc-44b10d78d4ac" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="689" height="60" alt="image" src="https://github.com/user-attachments/assets/6a9b31c2-b18a-44ea-8f96-b7c867642e9f" />



seq 10 
## OUTPUT

<img width="692" height="205" alt="image" src="https://github.com/user-attachments/assets/3bb31120-8872-48fd-a9c4-3092a6df3504" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="691" height="78" alt="image" src="https://github.com/user-attachments/assets/31c22e93-d083-4f12-b7ff-b0f65bb82db5" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="691" height="78" alt="image" src="https://github.com/user-attachments/assets/493ecfaf-550c-49db-8c0b-d7eadd4a3385" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="691" height="100" alt="image" src="https://github.com/user-attachments/assets/d236e37a-9ced-4f26-abc0-c0d6f693f962" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="647" height="86" alt="image" src="https://github.com/user-attachments/assets/6ddb73c1-a2e7-45b2-8d09-3b91486999f7" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="647" height="86" alt="image" src="https://github.com/user-attachments/assets/871c2d79-510e-4be5-a657-2635ee2868bd" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="681" height="84" alt="image" src="https://github.com/user-attachments/assets/59dc04ce-c7b4-4dd9-ab66-345bbca53048" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="681" height="84" alt="image" src="https://github.com/user-attachments/assets/4090e89b-0a5f-41b3-a2c1-d5c02ef8342f" />

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
<img width="684" height="118" alt="image" src="https://github.com/user-attachments/assets/1af47ca9-54a6-4e9e-8ce1-207fb00d3310" />


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
<img width="684" height="118" alt="image" src="https://github.com/user-attachments/assets/0efd8341-186a-4c40-b404-8798e7a1174e" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
## OUTPUT
<img width="737" height="166" alt="image" src="https://github.com/user-attachments/assets/2e8c5ddf-4a27-49f8-b1c1-c8f9e49838bc" />




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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



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
![433067988-e4af163e-b80a-40fc-bcf1-fa93109286af](https://github.com/user-attachments/assets/84953d19-b787-4d04-a8c3-a19a085ae3f5)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![433068052-14ac7075-3b09-4e91-add5-3456bb13fc66](https://github.com/user-attachments/assets/40b450be-bec8-4562-a880-c450939f6729)

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
![433068530-b953a2f3-5513-4a29-9de6-431e1489c581](https://github.com/user-attachments/assets/debbba16-b7c8-46ce-b86c-cb798492563e)

 
ls file1
## OUTPUT
![433068620-e988dd15-3557-4cdc-9c5a-56afc6dc70ce](https://github.com/user-attachments/assets/97098a87-4f4d-4ae6-97d4-6d0889b3f129)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![433068778-d39c5f62-2db3-4955-84c9-6f954d50ae18](https://github.com/user-attachments/assets/a2b93b30-9816-4608-932c-e62816a84d08)

 
abcd
 
echo $?
 ## OUTPUT
![433069355-a7d96713-1af4-4dcf-ab74-70411b23153f](https://github.com/user-attachments/assets/1155a135-60a3-49cb-85a4-98f5cdd1ac45)


 
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

![433070377-b10f44ee-7d68-4422-af94-d333b28feff2](https://github.com/user-attachments/assets/f2f67ff0-93b1-47de-b835-94dd62c89625)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![433070842-fdc676c2-30b4-4cb5-856a-0f8a4ad6e040](https://github.com/user-attachments/assets/47e8867b-4412-4a6b-990d-fed61cb49dc8)



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
![433070842-fdc676c2-30b4-4cb5-856a-0f8a4ad6e040](https://github.com/user-attachments/assets/f67462c8-405b-4d51-b278-1f6513f455b0)

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

![433071221-005816e4-afad-4995-9435-ee00da64d1fd](https://github.com/user-attachments/assets/a74eca48-c272-4323-8563-44bcbfcfc715)


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
![433071458-4ef6ef44-0b5f-48ac-a075-9ba22be5807d](https://github.com/user-attachments/assets/ceabd713-451c-4573-b607-302b23b6eed7)


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
![433072032-a8130528-2907-4ace-9b34-4a1d6f314c66](https://github.com/user-attachments/assets/60989f38-9c3d-4c3f-a5c2-47e7ee5c2fe7)


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
![433072331-ab09b9e2-280f-4fe8-8351-91a7a6c74c85](https://github.com/user-attachments/assets/a20cb91e-5c82-4cdc-8676-f86a6d5479df)


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
![433072604-fef988a9-668c-4c57-9390-06195de6ec87](https://github.com/user-attachments/assets/a2a1fa20-ab48-45aa-b93a-fed3a3310f34)

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
![433074655-7c63c81f-e699-4029-ad04-5b32b616f33c](https://github.com/user-attachments/assets/692694c1-c08c-46de-9e0b-e46aaf711fe5)

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
![433079518-a137aaa7-9661-49c3-b4a6-eb739bd0e876](https://github.com/user-attachments/assets/202b1e17-0d91-4d63-a465-1768cffec29b)


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
![433079648-3072743a-9691-40b4-99ab-5d9189afd9ea](https://github.com/user-attachments/assets/d7de662f-ee3c-4a83-948e-49aa016f275a)

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
![433079699-17775c12-db30-4953-8c3e-1c80482a0cd3](https://github.com/user-attachments/assets/790bdcee-63eb-4fcd-902d-4e5196cb71b0)

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
 ![433079778-88560eb0-ff33-47e4-81bb-88d413240e20](https://github.com/user-attachments/assets/17ad8470-7aa4-4a2a-9d43-d74dd7db87f1)


 
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
 ![433080335-295e60f5-4274-4953-a0df-f0881c625371](https://github.com/user-attachments/assets/213f2fe7-c200-423e-bbda-a0a472eb8c99)

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

![433080473-482c630c-3b9b-42d1-8f95-dcdb431ce8bd](https://github.com/user-attachments/assets/fab37407-b4fe-4e19-8b3e-26d8b2e108e4)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![433080514-a307d5a2-dcea-4379-8a73-4d19df5e70a6](https://github.com/user-attachments/assets/7f6e8618-5d66-4268-bc1c-a47a0af657ba)


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
![433080583-4c206ec8-5809-40bb-8a55-3f72201ffb24](https://github.com/user-attachments/assets/057858f2-961b-401a-a630-c1cd86dc4761)

 
 ./funcex.sh 1 2
![433080610-5355b55a-8615-41eb-b2d6-1291bd114e7a](https://github.com/user-attachments/assets/b0ce8ec1-0b10-494a-b950-b637ce5f2b9d)

 
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


 ![433080680-dd025c0c-d7c2-4882-840e-4070d5e4644b](https://github.com/user-attachments/assets/3e7a27e7-377d-4835-810b-f949d8525cd2)

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

![433080803-e4709e9d-080d-4670-b104-e6616064ce80](https://github.com/user-attachments/assets/096eacd3-7d26-4766-a801-fe72352a9c7c)


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
 
 ![433080889-77fa2545-28db-4def-a70f-2e4d1dae8f1a](https://github.com/user-attachments/assets/c645bea3-c8a1-48a7-9d78-031c9ba4b021)

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
 ![433081120-209171aa-f009-4f76-b623-c8b364c8f21a](https://github.com/user-attachments/assets/1ea4aea2-8868-4f08-99c7-ec4653eaab8b)

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
![433081217-c67d9c34-9a34-4dba-a619-589ee9ceca73](https://github.com/user-attachments/assets/d7eb5a4f-f597-4d3f-9e9a-ac93356b3fe7)


# RESULT:
The Commands are executed successfully.
