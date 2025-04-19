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
// git add-h
// git commit
// git origin

### Display the content of the files
cat < file1


## OUTPUT

![Screenshot 2025-04-19 141317](https://github.com/user-attachments/assets/c0a59b04-5b20-403f-9aa5-e3a6230f0d2f)



cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/636daa5b-2418-46b3-9aa6-3f808bb04667)


# Comparing Files
cmp file1 file2
## OUTPUT


![image](https://github.com/user-attachments/assets/700e7a60-fd4b-49b3-8802-31705a1eff3b)

 
comm file1 file2
 ## OUTPUT

![image](https://github.com/user-attachments/assets/e28f5de8-d6de-4e8e-a50a-7a438a790290)


 
diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/ef2e0ccd-ddd5-43ca-9162-2bb2467c925b)



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

![image](https://github.com/user-attachments/assets/15bdb22e-5e6b-419d-b884-b2a7791d0a80)


cut -d "|" -f 1 file22
## OUTPUT


![image](https://github.com/user-attachments/assets/c5c6e083-ba0f-47ba-a8fb-c2e0fea2a067)



cut -d "|" -f 2 file22
## OUTPUT


![image](https://github.com/user-attachments/assets/974539ae-4132-4fbe-87f0-0709b1a8dcb9)



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

![image](https://github.com/user-attachments/assets/69f9df64-86b6-4f03-be60-c24a54251d39)



grep hello newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/adc82d49-e857-494f-a14d-714fe9cc2aae)


grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/57b52905-c8b4-4693-b033-95f512514edd)


cat newfile | grep -i "hello"
## OUTPUT


![image](https://github.com/user-attachments/assets/ebbc2d7e-6f35-44ce-bb5d-25dff2b660f0)


cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/559b16fc-c37f-4126-bf87-0e46311d65ab)



grep -R ubuntu /etc
## OUTPUT


![image](https://github.com/user-attachments/assets/e5d3aa48-3ef0-4ecf-9edd-d4d5d8f864b2)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/15624f87-acd4-4db3-b216-863aca7180e9)

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


![image](https://github.com/user-attachments/assets/06bdea88-4552-4e86-b2c4-35f3f248f505)



egrep -w '(H|h)ello' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/bd8bfb99-8b71-4e4d-927f-a7dfa8b931eb)




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/ca792eaf-718d-4411-becb-db0e2e076e38)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/fb2c3f08-a196-4166-96c3-28774a63eeec)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/a91ed792-16bf-462f-996e-659148f49377)



egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/53c1161a-bc11-4286-aaab-84ccf7ed0072)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/f5aa3cad-317c-43ce-899f-f6cc2244ff86)



egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/6e6beaeb-c577-49b4-a5f5-cc5204336dc5)

egrep 'Linux.*world' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/74994095-3a9e-4ae2-b2c3-305cf6d75548)


egrep 'Linux.*World' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/5af6e9f5-3b24-4439-aec8-a52ab5c3c4b4)



egrep l{2} newfile
## OUTPUT


![image](https://github.com/user-attachments/assets/df46a6c4-3428-4ed1-97ae-e478f1d88ac8)



egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/user-attachments/assets/ab7fdf08-8a3b-495c-8dbf-604fe17b889f)

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

![image](https://github.com/user-attachments/assets/658dc148-aeda-46d5-8b56-5b2a280edcdc)


sed -n -e '$p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/6ccc8a34-d561-4d6c-b5cf-4c8aee26e736)


sed  -e 's/Ram/Sita/' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/f60cc4e1-f303-491a-92a5-cebf405f9976)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/4a94024c-b108-4413-bb45-f39e1f5315cf)



sed  '/tom/s/5000/6000/' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/93624ed0-5c9c-4b97-861e-c0c5c7367bc0)


sed -n -e '1,5p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/ecf49a64-9ef4-4175-8712-ab49f9e74a3f)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/d51bacd9-e1a8-4f14-b742-fa45a3a11e1c)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/6113cab9-0b66-469d-9ccf-9c401e3721e4)


seq 10 
## OUTPUT


![image](https://github.com/user-attachments/assets/c54319a3-2913-46f4-b0f2-a699dcbc960c)


seq 10 | sed -n '4,6p'
## OUTPUT


![image](https://github.com/user-attachments/assets/d8c6d0d4-4397-4a0e-bfc4-1e7746562a4c)



seq 10 | sed -n '2,~4p'
## OUTPUT


![image](https://github.com/user-attachments/assets/dc47e19b-6669-479c-985f-657eaa5058d4)



seq 3 | sed '2a hello'
## OUTPUT


![image](https://github.com/user-attachments/assets/3a738dc1-a6da-4c12-80d2-407715508e49)



seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/baa9286d-a1ca-474f-94e1-4324396275ae)


seq 10 | sed '2,9c hello'
## OUTPUT


![image](https://github.com/user-attachments/assets/c8486548-50c2-4995-ad8b-d08b740f0fef)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/a28012fd-1c00-483c-ba54-39f62990c49f)



sed -n '2,4{s/$/*/;p}' file23

![image](https://github.com/user-attachments/assets/2fdff45f-9b1d-40df-abc6-803659883872)


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

![image](https://github.com/user-attachments/assets/2a31ba89-a2f8-4dd4-912f-87fcccfeda6a)

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
![alt text](img/uniq.png) 


![image](https://github.com/user-attachments/assets/5c1f7a40-739c-4ec6-a38d-4c39b968f5e1)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/user-attachments/assets/88e41b6b-3c91-4f5d-869f-c2b9bbe2a167)


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


![image](https://github.com/user-attachments/assets/403174c6-81f9-4bf1-a81e-3cfa63261b93)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/c0f668d6-e39b-4ec2-8bc0-b0f9a46a2873)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

\![image](https://github.com/user-attachments/assets/492a16cb-1009-4235-9e7f-22f4f147bf51)


![image](https://github.com/user-attachments/assets/5de1a3de-e01b-466b-a4cf-c313dc67f0c3)

mkdir backupdir
 
mv backup.tar backupdir
 
## OUTPUT

![image](https://github.com/user-attachments/assets/fb99d2e6-f39c-495c-b172-e9dc49eeaaeb)

![image](https://github.com/user-attachments/assets/772be2c9-52d1-4e0d-aad5-fe4ba562b34a)


tar -xvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/762d31f2-3365-4300-b3bd-81eb5214be4f)

![image](https://github.com/user-attachments/assets/09d4936b-4dc7-4b0f-b946-25ba745ecab7)


gzip backup.tar

ls .gz
## OUTPUT


![image](https://github.com/user-attachments/assets/630c82ec-b0da-4bc7-b9bf-b52d8e97c92a)


gunzip backup.tar.gz
## OUTPUT

![image](https://github.com/user-attachments/assets/3162b2d6-557d-4205-9058-4d4bee4186e6)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World'; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/user-attachments/assets/cb6b9e90-53dd-452c-8233-b9f105e53436)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/5fcfc1d6-fc9e-4898-b2d5-dcc736474c5a)

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

![image](https://github.com/user-attachments/assets/d98a8540-7f4e-443d-9f0b-eb4bdf46ef7c)

 
ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/f949733d-4335-4573-a59d-ff9839403bec)

## OUTPUT 


![image](https://github.com/user-attachments/assets/78b7b8e3-4df1-4795-9536-29e7b48c8f65)


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

![image](https://github.com/user-attachments/assets/7c4a2bda-2162-4f54-9fa4-1d14115da47f)


abcd
 
echo $?
## OUTPUT


![image](https://github.com/user-attachments/assets/ce81c949-b1ca-49b0-910d-3ce97342b559)

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

![image](https://github.com/user-attachments/assets/f4cd8917-4591-46a8-abad-54d70929eb89)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


![image](https://github.com/user-attachments/assets/0ff6fb14-ba84-4408-be73-37d5dda5b2f4)


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


![image](https://github.com/user-attachments/assets/47235c70-901c-46b2-9fc6-fa3d4597acbb)

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


![image](https://github.com/user-attachments/assets/923a4ef6-20f9-47f5-a8e6-21dfc06c48ac)


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


![image](https://github.com/user-attachments/assets/3f383bc2-8ac5-4542-a4d8-afc4e9120321)

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

![image](https://github.com/user-attachments/assets/68562705-6f1f-48d7-af8e-fbe1eb83d27b)


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

![image](https://github.com/user-attachments/assets/1e5c2941-48ae-4d9c-86a3-f6baca102507)


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


![image](https://github.com/user-attachments/assets/97e45919-c5d8-46e5-83ff-2211e3df08d2)


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
## OUTPUT

![image](https://github.com/user-attachments/assets/87a612fe-64b1-4ce1-8748-eb8a5e5b5bbb)


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
## OUTPUT

![Screenshot 2025-04-19 150438](https://github.com/user-attachments/assets/c2d74101-0211-4694-b3c7-6a94da418fc7)


 
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
$ ./untiltest.sh
## OUTPUT

![image](https://github.com/user-attachments/assets/d671a7db-31d3-403d-8333-506f26a1746c)

 
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

![image](https://github.com/user-attachments/assets/ae0bc99c-ba8a-4ea5-a246-4cbdf198974b)

 
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

![image](https://github.com/user-attachments/assets/df464ea0-3e66-44eb-b434-9f04e2116d11)

 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```

$ chmod 755 forin3.sh
$ ./forin3.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/3f231105-c591-4268-a176-7548c9406716)


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

cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

$ chmod 777 forinfile.sh
$./forinfile.sh
## OUTPUT

![image](https://github.com/user-attachments/assets/76fe42ad-bc9d-40eb-ab4d-ec7b11a41ae1)

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

![image](https://github.com/user-attachments/assets/5d02ebda-673c-401c-98e7-b02be163979a)


cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype1.sh
$ ./forctype1.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/2249758b-d9f5-4c37-9a75-912060074c9a)


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

![image](https://github.com/user-attachments/assets/f366b25f-2da1-4b72-86ee-8577cac67962)

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

![image](https://github.com/user-attachments/assets/db614d73-d579-442e-bdcf-e4ffe65b6d1d)

 
cat forcontinue.sh 
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
echo "The for loop is completed"
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/41f677dd-9791-4813-b0c6-95ed73f4e91f)


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

![image](https://github.com/user-attachments/assets/6cd46e29-b78d-4f96-b164-615eb4150715)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. "
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT



![image](https://github.com/user-attachments/assets/4686d62b-f5ac-4ac6-8a45-64a870e69a96)


 
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

![image](https://github.com/user-attachments/assets/92ae1b37-e60e-4aaf-be37-b9d35b863c34)

 
 ./funcex.sh 1 2

![image](https://github.com/user-attachments/assets/3c9f049e-f996-487c-b4b5-112f3065b051)

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

![image](https://github.com/user-attachments/assets/8f5d1d9c-45cb-4a20-9e17-dc28ceb41a7b)


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
$ chmod 777 argshift1.sh
## OUTPUT
$ ./argshift1.sh 1 2 3

![image](https://github.com/user-attachments/assets/95426b83-307c-4d79-8d17-c4b55a75e30c)


cat argshift3.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +xch
```
## OUTPUT
 ./argshift3.sh 1 2 3

 ![image](https://github.com/user-attachments/assets/bc575dbd-bb14-4c54-91ae-a70ebd250655)

 
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

![image](https://github.com/user-attachments/assets/b1e275ab-3a9c-46dc-809c-1da7a9a2a56a)

 
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

![image](https://github.com/user-attachments/assets/ad0677ae-0de0-4e06-aeed-946420297b73)


# RESULT:
The Commands are executed successfully.
