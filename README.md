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

![Screenshot 2025-04-20 143052](https://github.com/user-attachments/assets/ff3b6595-c23a-4bee-b39a-0fe6ddc7d8c0)


grep -v hello newfile 
## OUTPUT

![Screenshot 2025-04-20 143102](https://github.com/user-attachments/assets/a39d7477-e474-4c34-80d4-9a8db7e01c81)


cat newfile | grep -i "hello"
## OUTPUT
![Screenshot 2025-04-20 143204](https://github.com/user-attachments/assets/741961a0-a1c3-435c-bf7c-d97bd4107e3e)




cat newfile | grep -i -c "hello"
## OUTPUT


![Screenshot 2025-04-20 143504](https://github.com/user-attachments/assets/663caa43-653c-478d-8178-6e72608deff9)



grep -R ubuntu /etc
## OUTPUT

![Screenshot 2025-04-20 143521](https://github.com/user-attachments/assets/1145616c-2adc-4591-848d-a30add0acbec)



grep -w -n world newfile   
## OUTPUT
![Screenshot 2025-04-20 143538](https://github.com/user-attachments/assets/672b9d02-144c-4a4b-bb0f-6ff665acfba0)



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

![Screenshot 2025-04-20 143554](https://github.com/user-attachments/assets/1bd6ff72-5fbb-4b87-8e42-bbbe0baca7b5)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![output1_17](https://github.com/user-attachments/assets/192077a7-a53f-4302-8f14-e6860da78750)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![output1_18](https://github.com/user-attachments/assets/e9a63fea-de3e-4825-aab3-8b479e391d6e)



egrep '(^hello)' newfile 
## OUTPUT

![output1_19](https://github.com/user-attachments/assets/5664908e-2505-46ec-a784-d9e4cafb2d6c)


egrep '(world$)' newfile 
## OUTPUT

![output1_20](https://github.com/user-attachments/assets/844f0685-aad2-406b-8e1d-0213f8ffe5f6)


egrep '(World$)' newfile 
## OUTPUT
![output1_21](https://github.com/user-attachments/assets/49f1e57d-d82e-4c70-8ea3-21ce18511995)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![output1_22](https://github.com/user-attachments/assets/739fadf3-3b20-4653-b22e-81be2fa3e5f2)



egrep '[1-9]' newfile 
## OUTPUT

![output1_23](https://github.com/user-attachments/assets/0ccd74c9-fea7-4306-8afc-b737408db919)


egrep 'Linux.*world' newfile 
## OUTPUT
![output1_24](https://github.com/user-attachments/assets/549a928a-564b-443b-9390-97efd236ab06)


egrep 'Linux.*World' newfile 
## OUTPUT
![output1_25](https://github.com/user-attachments/assets/bf84c609-7378-4550-b978-567c71b8d1f2)


egrep l{2} newfile
## OUTPUT

![output1_26](https://github.com/user-attachments/assets/1379d26e-e740-483a-ab5f-616ee27c77e5)


egrep 's{1,2}' newfile
## OUTPUT 
![output1_27](https://github.com/user-attachments/assets/3768546a-cb2e-4c2c-87ef-e682eedd26bf)


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

![output1_29](https://github.com/user-attachments/assets/08cd886b-03a8-4fab-9150-3b6472db0db7)


sed -n -e '$p' file23
## OUTPUT

![output1_29](https://github.com/user-attachments/assets/381adfe1-9568-494b-b775-1a43de3143be)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![output1_30](https://github.com/user-attachments/assets/f4e6e441-4d87-45fc-8748-a4ee10a4c968)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


![output1_30](https://github.com/user-attachments/assets/da4d7bfc-4333-4725-9dff-884cd65aa896)

sed  '/tom/s/5000/6000/' file23
## OUTPUT
![output1_32](https://github.com/user-attachments/assets/e1813d9b-f44c-416a-b5ed-240f93bd08c3)


sed -n -e '1,5p' file23
## OUTPUT

![output1_33](https://github.com/user-attachments/assets/5dd0a520-6523-46c5-9bb0-0e3e3083ca50)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![output1_34](https://github.com/user-attachments/assets/9fefd117-4503-4e90-8167-d153c3cee5e3)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![output1_35](https://github.com/user-attachments/assets/f8198dc9-ea66-41ff-a653-0a877822594a)


seq 10 
## OUTPUT

![output1_36](https://github.com/user-attachments/assets/bcfa9fe5-2b30-436a-a930-07db34d49763)


seq 10 | sed -n '4,6p'
## OUTPUT

![output1_37](https://github.com/user-attachments/assets/05911e96-71f0-451c-9bda-94c73d205167)


seq 10 | sed -n '2,~4p'
## OUTPUT

![output1_38](https://github.com/user-attachments/assets/b302f47c-c313-4da4-9c87-d569645e7daa)


seq 3 | sed '2a hello'
## OUTPUT
![output1_39](https://github.com/user-attachments/assets/89e24150-c119-4936-95bc-6be8531bf7ea)



seq 2 | sed '2i hello'
## OUTPUT

![output1_40](https://github.com/user-attachments/assets/e5bd6a8b-50b3-4f21-bf17-c2c4e55f2ff1)

seq 10 | sed '2,9c hello'
## OUTPUT

![output1_41](https://github.com/user-attachments/assets/027e69e0-8dd7-4a58-b7c8-b042eb4fb600)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![output1_42](https://github.com/user-attachments/assets/841a383c-d628-46de-bf7e-af480246e3f5)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![output1_43](https://github.com/user-attachments/assets/f10dfa2b-73a0-4406-9b66-34137573a54a)

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
![output1_44](https://github.com/user-attachments/assets/38220970-a371-4a26-8122-0a9e9ac6a151)


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
![output1_45](https://github.com/user-attachments/assets/70b3d913-0569-4b01-b28a-5d7396530b95)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![output1_46](https://github.com/user-attachments/assets/51bc0aa4-ac10-424b-8238-c1a9acf44764)

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

![output1_47](https://github.com/user-attachments/assets/caab8dc1-8458-45db-b0b0-49131c2fd726)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![output1_48](https://github.com/user-attachments/assets/d557cc0b-3fdb-4d49-9474-4a22bc2017ab)

#Backup commands
tar -cvf backup.tar *
## OUTPUT

![output1_49](https://github.com/user-attachments/assets/0fe7b3cb-8521-4205-b86a-9fa6acc6e2c8)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![output1_50](https://github.com/user-attachments/assets/ff5c84bb-c61d-430a-933d-94b7614cfd6f)


tar -xvf backup.tar
## OUTPUT

![output1_51](https://github.com/user-attachments/assets/3c8e10c6-4272-4cda-b8c4-2b9219be64bb)

gzip backup.tar

ls .gz
## OUTPUT
![output1_52](https://github.com/user-attachments/assets/2bff62d4-69fd-4986-8b2b-94ac373e32bf)

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
![output1_54](https://github.com/user-attachments/assets/302361b2-3756-4826-bbab-0fb87a047afa)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![output](./output1_55.png)

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
![output1_56](https://github.com/user-attachments/assets/ca4e4433-4f7a-42f3-aaeb-4327a0b409e0)

 
ls file1
## OUTPUT
![output1_57](https://github.com/user-attachments/assets/206f3803-8d5a-47b1-afd7-b444e8691dee)

echo $?
## OUTPUT 
![output1_58](https://github.com/user-attachments/assets/913aa257-0d7c-4102-b037-168c70c21302)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![output1_59](https://github.com/user-attachments/assets/bc225b5e-b151-4b4f-98d2-3c276d8b7521)

abcd
 
echo $?
 ## OUTPUT
![output1_60](https://github.com/user-attachments/assets/86d2b48a-1e43-4c8b-b907-9dd5e93440e7)


 
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


![output1_61](https://github.com/user-attachments/assets/cba96cf5-2aa5-485d-b1ad-7729f21ef051)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![output1_62](https://github.com/user-attachments/assets/2b0f1685-c020-48b2-9126-f5d03544b51c)

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
![output1_63](https://github.com/user-attachments/assets/95b3fae5-afbf-4b6a-95fc-b3e755e0231c)


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

![output1_64](https://github.com/user-attachments/assets/3128e17f-4a46-42e9-b6ef-9ed5b1b34674)


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
![output1_65](https://github.com/user-attachments/assets/7e77dc89-63b1-450e-9af3-f5dad61b10e3)

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
![output1_66](https://github.com/user-attachments/assets/88e1a96e-233f-4c4b-a132-e1ea96637326)

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
![output1_67](https://github.com/user-attachments/assets/a78b1cc9-182f-425b-b6f7-aa94cdb5b3f5)


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
![output1_68](https://github.com/user-attachments/assets/40229f75-65df-46ad-baf6-1409dec7ff77)

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

![output1_69](https://github.com/user-attachments/assets/bee097e4-0d15-453e-b393-b56c26fb210e)

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

 ![output1_70](https://github.com/user-attachments/assets/18327ae7-3ac4-4635-a72e-05cc12e1e2a8)

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
![output1_71](https://github.com/user-attachments/assets/106275f2-c7db-4b41-a38a-668a18b0169e)

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
![output1_72](https://github.com/user-attachments/assets/581312db-2fce-49fe-9b3e-e44c9d98bbe1)

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
![output1_73](https://github.com/user-attachments/assets/43d31946-c4c8-4ec8-a164-e076fab75d02)

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
![output1_74](https://github.com/user-attachments/assets/535ce88e-558d-4e7d-af99-860cbd6624c2)

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
![output1_75](https://github.com/user-attachments/assets/86f43ac9-fb26-44fd-97bd-075e4705a186)


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

![output1_76](https://github.com/user-attachments/assets/737ed7f6-c7b7-4d34-8c7d-6ec108206e70)

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

 ![output1_77](https://github.com/user-attachments/assets/d83a5ec7-064d-46eb-978c-580d6d897e21)

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
![output1_78](https://github.com/user-attachments/assets/271a5c58-12aa-4932-8110-762f77f11119)

 
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
![output1_79](https://github.com/user-attachments/assets/d6ff95c3-806b-4dd7-b60f-0a031c3ad1e2)


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

![output1_80](https://github.com/user-attachments/assets/f4298035-31df-4d30-94d6-7bd865bfb0b0)

 
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

![output1_81](https://github.com/user-attachments/assets/7bb71b61-3373-49cc-b741-ee36722dada8)

 
 ./funcex.sh 1 2

## OUTPUT
![output1_82](https://github.com/user-attachments/assets/e782dbdf-8c61-4163-88d7-fe60646edc44)

 
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
![output1_83](https://github.com/user-attachments/assets/b0b0299e-f276-49b8-8ebd-331e9f3dd1cd)


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
![output1_84](https://github.com/user-attachments/assets/b1955fb6-f2e5-4678-8252-81c5393c1ed4)

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
![output1_84](https://github.com/user-attachments/assets/c58a7cb9-9706-472c-be5e-5e787dd1f34e)


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
![output1_86](https://github.com/user-attachments/assets/3ef5a121-8309-4117-a9db-65d6fa693ce8)

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
![output1_87](https://github.com/user-attachments/assets/493196a5-f3c9-4814-aa12-2d4dcb57430f)


# RESULT:
The Commands are executed successfully.
