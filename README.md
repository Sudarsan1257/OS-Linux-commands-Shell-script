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

![Screenshot 2025-04-20 141425](https://github.com/user-attachments/assets/3af8d1fd-db6d-4c6e-929a-8baf0daeaa27)


cat < file2
## OUTPUT
![Screenshot 2025-04-20 141618](https://github.com/user-attachments/assets/4fd80b76-6b3c-4c1c-b6bf-49588574bf59)



# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2025-04-20 142145](https://github.com/user-attachments/assets/a0670697-17d7-4457-a02b-abaf793254cf)


comm file1 file2
 ## OUTPUT
![Screenshot 2025-04-20 142210](https://github.com/user-attachments/assets/4b060921-8c57-40fd-8517-1dbb9d0d2cdd)


 
diff file1 file2
## OUTPUT

![Screenshot 2025-04-20 142228](https://github.com/user-attachments/assets/90c15bc2-639b-49ea-b05a-0d90cd795e4d)


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
![Screenshot 2025-04-20 142523](https://github.com/user-attachments/assets/7eb18e29-2b2a-4a01-acb1-a6ec6abfa7ba)





cut -d "|" -f 1 file22
## OUTPUT
![Screenshot 2025-04-20 142555](https://github.com/user-attachments/assets/28aab90d-4f38-4bdc-beea-6de1ed9fa40d)




cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2025-04-20 142742](https://github.com/user-attachments/assets/4b77270c-273b-4e32-9168-5967a7b118cc)



cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
```
Hello world
hello world
 ```
grep Hello newfile 
## OUTPUT
![Screenshot 2025-04-20 142949](https://github.com/user-attachments/assets/2ac5ef1e-d925-4ef0-8b6d-e94efc2d13da)



grep hello newfile 
## OUTPUT
![Screenshot 2025-04-20 160538](https://github.com/user-attachments/assets/6444f084-9309-4b43-ad39-e577900310e0)




grep -v hello newfile 
## OUTPUT
![Screenshot 2025-04-20 160656](https://github.com/user-attachments/assets/5d6cb922-3ed4-4acd-ac76-adf9c7c58959)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot 2025-04-20 143052](https://github.com/user-attachments/assets/10f530ad-1200-42a5-b20b-ebb73b38be8c)




cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot 2025-04-20 160950](https://github.com/user-attachments/assets/c89de0c1-29d0-4f69-b721-3becc48e3aae)





grep -R ubuntu /etc
## OUTPUT

![Screenshot 2025-04-20 143521](https://github.com/user-attachments/assets/1145616c-2adc-4591-848d-a30add0acbec)



grep -w -n world newfile   
## OUTPUT


![Screenshot 2025-04-20 143204](https://github.com/user-attachments/assets/e5110cfd-e1ac-450f-9287-629e54e42419)


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

![Screenshot 2025-04-20 143504](https://github.com/user-attachments/assets/ccf9ecc3-1e8e-4497-9066-37235b634308)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot 2025-04-20 143521](https://github.com/user-attachments/assets/79cca6cc-791f-41f2-992b-995cf2d44054)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot 2025-04-20 143538](https://github.com/user-attachments/assets/15cc2eed-0712-4691-895f-b0babe8d4350)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot 2025-04-20 143554](https://github.com/user-attachments/assets/5d6e89e1-4e8b-4192-a096-c7dd1195bed2)



egrep '(world$)' newfile 
## OUTPUT

![Screenshot 2025-04-20 143616](https://github.com/user-attachments/assets/b7441b9a-02af-4e44-96f3-a9708a738cf0)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot 2025-04-20 143640](https://github.com/user-attachments/assets/af96759f-0e7d-43a6-beae-7d018cc0e96f)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot 2025-04-20 143659](https://github.com/user-attachments/assets/baa69278-552b-4583-af90-ecde5dbb6edc)




egrep '[1-9]' newfile 
## OUTPUT

![Screenshot 2025-04-20 143718](https://github.com/user-attachments/assets/39e393e9-63b5-443e-8018-f516955e2b4f)



egrep 'Linux.*world' newfile 
## OUTPUT

![Screenshot 2025-04-20 143735](https://github.com/user-attachments/assets/1eb456c5-0961-4a6f-82bb-f91f7ae8ef7c)



egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot 2025-04-20 143752](https://github.com/user-attachments/assets/cce0b273-9be1-409e-97cb-f4a504ebb95f)


egrep l{2} newfile
## OUTPUT

![Screenshot 2025-04-20 143811](https://github.com/user-attachments/assets/483cab61-8f08-4cee-9565-4ee2f541f9d9)



egrep 's{1,2}' newfile
## OUTPUT 

![Screenshot 2025-04-20 143829](https://github.com/user-attachments/assets/b741611d-2404-41f8-a30f-f3f1acdcd5be)



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

![Screenshot 2025-04-20 144128](https://github.com/user-attachments/assets/473e5d3f-4f8a-4648-8e9d-3a68831909a8)


sed -n -e '$p' file23
## OUTPUT

![Screenshot 2025-04-20 144156](https://github.com/user-attachments/assets/f66de60a-c294-4fb0-a82a-f7ea0dc8a24a)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot 2025-04-20 144217](https://github.com/user-attachments/assets/9f470944-98d4-449c-a9ae-18129d3587de)




sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot 2025-04-20 144239](https://github.com/user-attachments/assets/1857d489-341d-4671-9a42-39626582e2e2)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot 2025-04-20 144300](https://github.com/user-attachments/assets/6d652c90-1867-4deb-aa55-3b5a521efa1c)


sed -n -e '1,5p' file23
## OUTPUT
![Screenshot 2025-04-20 144316](https://github.com/user-attachments/assets/05cc815f-4e2a-4941-aacf-7ffb11c9cb5b)




sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot 2025-04-20 144336](https://github.com/user-attachments/assets/897f5897-892c-4df4-889c-12930f86b314)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot 2025-04-20 144352](https://github.com/user-attachments/assets/2881e2d6-d61d-438b-ae2e-a750bb6a3c41)



seq 10 
## OUTPUT

![Screenshot 2025-04-20 144411](https://github.com/user-attachments/assets/37eae785-16d5-4647-a0e4-8e9e2105219f)



seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot 2025-04-20 144431](https://github.com/user-attachments/assets/f092af69-1bb8-4c58-8036-e51f0eddf627)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot 2025-04-20 144527](https://github.com/user-attachments/assets/6aa7d8cf-6e5e-497a-982f-0dc9441db21f)




seq 3 | sed '2a hello'
## OUTPUT

![Screenshot 2025-04-20 144548](https://github.com/user-attachments/assets/2ff3d687-0faf-4118-8282-08463eab4928)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot 2025-04-20 144607](https://github.com/user-attachments/assets/8712b33f-4308-4314-af2b-29e6e558dae7)



seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot 2025-04-20 144631](https://github.com/user-attachments/assets/8e7480c8-6a98-416e-b2f0-193aeaa4d2ec)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot 2025-04-20 144704](https://github.com/user-attachments/assets/9061e816-c88d-4588-8ff3-d006c508c041)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Screenshot 2025-04-20 144704](https://github.com/user-attachments/assets/54808571-411a-41ed-9110-ca84da396738)



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

![Screenshot 2025-04-20 144832](https://github.com/user-attachments/assets/5548cff6-524d-476c-a6f6-410e0a245f4f)


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
![Screenshot 2025-04-20 145015](https://github.com/user-attachments/assets/0e128d32-3a9c-468d-be1f-e436b068b138)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot 2025-04-20 145035](https://github.com/user-attachments/assets/01e8fbd5-45e4-4b31-81b3-8d07af1adfcd)


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

![Screenshot 2025-04-20 145149](https://github.com/user-attachments/assets/3edaba30-5c9e-4098-a1a1-c3b978aa6186)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot 2025-04-20 145208](https://github.com/user-attachments/assets/81ba2640-020c-4b3d-96ba-2c06b4266d75)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot 2025-04-20 155203](https://github.com/user-attachments/assets/5eef02ab-faab-443d-927b-b961b717812a)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot 2025-04-20 145806](https://github.com/user-attachments/assets/8ee1fb93-ec94-4d5c-9458-b616457530c5)



tar -xvf backup.tar
## OUTPUT

![Screenshot 2025-04-20 145908](https://github.com/user-attachments/assets/d5a574ec-2ac9-4b16-9a67-7e7b5b902abf)


gzip backup.tar

ls .gz
## OUTPUT
![Screenshot 2025-04-20 150040](https://github.com/user-attachments/assets/09a81edd-d224-4bc6-8fd3-cf6ba5609e82)


gunzip backup.tar.gz
## OUTPUT
![output1_53](https://github.com/user-attachments/assets/e506c0f7-925d-4970-9368-3406782e0ede)

 
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
![Screenshot 2025-04-20 151239](https://github.com/user-attachments/assets/0503882f-007c-437f-a41c-9fa69637277c)


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
![Screenshot 2025-04-20 152032](https://github.com/user-attachments/assets/c77bb3d4-3f7d-4e00-ba9c-b80118fb96dd)


 
ls file1
## OUTPUT
![Screenshot 2025-04-20 151445](https://github.com/user-attachments/assets/36776043-c9c1-43ae-ae10-a8327a51794a)


echo $?
## OUTPUT 

![Screenshot 2025-04-20 151458](https://github.com/user-attachments/assets/b4d54192-162b-4764-a4a8-5b74caee8b70)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![output1_59](https://github.com/user-attachments/assets/bc225b5e-b151-4b4f-98d2-3c276d8b7521)

abcd
 
echo $?
 ## OUTPUT
![Screenshot 2025-04-20 151458](https://github.com/user-attachments/assets/3b2da665-5f30-4dc7-97e8-518d00fb7d8c)


 
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


![Screenshot 2025-04-20 152331](https://github.com/user-attachments/assets/0885c526-53dd-4340-baa4-512168123f78)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![Screenshot 2025-04-20 152405](https://github.com/user-attachments/assets/3499a5ed-7292-4932-8aa5-38959ef7ef74)

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
 chmod 755 psswdperm.sh

./psswdperm.sh
## OUTPUT

![Screenshot 2025-04-20 152622](https://github.com/user-attachments/assets/a82549d6-9890-4386-882b-c18059042923)



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
chmod 755 ifnested.sh

./ifnested.sh 
## OUTPUT

![Screenshot 2025-04-20 152913](https://github.com/user-attachments/assets/9e99a003-c8ee-4370-b072-081123938a0d)



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
![Screenshot 2025-04-20 153005](https://github.com/user-attachments/assets/5f53f1c2-3c1f-49d1-9d89-36404db08f17)


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
![Screenshot 2025-04-20 152808](https://github.com/user-attachments/assets/b0a4e5b0-4ab4-4545-b3dd-60293b312302)


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

![Screenshot 2025-04-20 153059](https://github.com/user-attachments/assets/ebc11bdd-15ee-4198-9892-c142836f5e4f)


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

![Screenshot 2025-04-20 153322](https://github.com/user-attachments/assets/d4d06dd3-225c-4290-b961-b3d89ee15f5a)

# using the case command
cat >casecheck.sh 
```bash
case $USER in Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";Rahim)
echo "Special testing account";gganesh)
echo "$USER, Do not forget to log off when you're done";*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
## OUTPUT

![Screenshot 2025-04-20 153410](https://github.com/user-attachments/assets/b577ef8b-615b-4108-9d72-dc94855a1a4f)

cat > whiletest.sh
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


![Screenshot 2025-04-20 153507](https://github.com/user-attachments/assets/00bf2c85-9ea0-4916-b092-66783ddde33e)

cat > untiltest.sh 
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

$ ./untiltest.sh
 ## OUTPUT
![Screenshot 2025-04-20 153546](https://github.com/user-attachments/assets/e0c088fd-7745-471e-986c-06144b4c755b)


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

$ ./forin1.sh
## OUTPUT

![Screenshot 2025-04-20 153647](https://github.com/user-attachments/assets/e9e56946-f2e5-416f-bad6-c75bdd1d5fca)

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
## OUTPUT
![Screenshot 2025-04-20 153755](https://github.com/user-attachments/assets/b9d79253-0866-4fb9-8433-0bdf8be81a84)


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

![Screenshot 2025-04-20 153850](https://github.com/user-attachments/assets/5a0c3e53-7747-413c-9519-004f42283d56)

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
![Screenshot 2025-04-20 153951](https://github.com/user-attachments/assets/e56b2f7e-f144-4d41-a85b-2437b4a1aba6)



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

![Screenshot 2025-04-20 154052](https://github.com/user-attachments/assets/ed25ca5c-a72e-40be-b48e-638a80582f81)


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
![Screenshot 2025-04-20 154156](https://github.com/user-attachments/assets/38e7039f-1591-4fdb-a77c-b14c4def80e5)


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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
![Screenshot 2025-04-20 154303](https://github.com/user-attachments/assets/3519f9ae-0b22-49a6-8360-e481aba769fe)


 
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
![Screenshot 2025-04-20 154419](https://github.com/user-attachments/assets/6bb62bac-4d18-4ff6-8a37-40bbb9055043)




 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program."
``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh
## OUTPUT
![Screenshot 2025-04-20 154528](https://github.com/user-attachments/assets/ce01d280-f080-4109-b87f-56c944d2441a)

 
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
 ./funcex.sh 

 ## OUTPUT

![Screenshot 2025-04-20 154639](https://github.com/user-attachments/assets/cc532a83-fa90-480a-b2c1-24c5b8a86cbb)


 
 ./funcex.sh 1 2

## OUTPUT

![Screenshot 2025-04-20 154708](https://github.com/user-attachments/assets/3fc91fd8-d071-4be8-ac1b-b558082f25f3)

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

$ ./argshift.sh 1 2 3
## OUTPUT

![Screenshot 2025-04-20 154805](https://github.com/user-attachments/assets/ebe4a8f4-a026-4589-8c24-f54637de374a)


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
![Screenshot 2025-04-20 154912](https://github.com/user-attachments/assets/e9966854-476e-4110-9352-7fbf23d53f26)


$ ./argshift.sh 1 2 3
## OUTPUT

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

 ./argshift.sh 1 2 3
## OUTPUT 
![Screenshot 2025-04-20 154952](https://github.com/user-attachments/assets/e0e8e2fb-b9fd-40a4-a2ac-9ac1587f05d0)



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
![Screenshot 2025-04-20 155042](https://github.com/user-attachments/assets/3845d6ca-cfb1-47c3-9348-625710f14290)


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
chmod 755 palindrome.sh

./palindrome.sh
## OUTPUT 
![Screenshot 2025-04-20 155131](https://github.com/user-attachments/assets/cf09fc1e-2c7b-4661-a59c-d5f858796ebf)



# RESULT:
The Commands are executed successfully.
