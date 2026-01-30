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
![WhatsApp Image 2026-01-30 at 8 30 30 AM](https://github.com/user-attachments/assets/c690085c-615d-417c-aefa-ce423def5a82)



cat < file2
## OUTPUT
![WhatsApp Image 2026-01-30 at 8 30 30 AM](https://github.com/user-attachments/assets/15917942-0d59-48cb-9818-ec4a40d11473)


# Comparing Files
cmp file1 file2
## OUTPUT
![WhatsApp Image 2026-01-30 at 8 30 31 AM](https://github.com/user-attachments/assets/9bc9eaab-ba17-4b4f-9e29-93288d41f4fc)

 
comm file1 file2
 ## OUTPUT
![WhatsApp Image 2026-01-30 at 8 30 31 AM (1)](https://github.com/user-attachments/assets/573f08ce-4e2a-4295-85ab-90b4e04dc345)

 
diff file1 file2
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 23 AM (4)](https://github.com/user-attachments/assets/63d8ed3d-524e-4aea-a676-27580e5b9eec)


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
![WhatsApp Image 2026-01-30 at 9 21 23 AM (5)](https://github.com/user-attachments/assets/18f2f4ad-8c75-41cd-9d0a-48730209d94f)





cut -d "|" -f 1 file22
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 23 AM (6)](https://github.com/user-attachments/assets/914ff811-8b8d-475e-93a0-1434f67a8849)



cut -d "|" -f 2 file22
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 23 AM (7)](https://github.com/user-attachments/assets/3548fe61-6acb-4125-b56a-4991770d255a)



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
![WhatsApp Image 2026-01-30 at 9 21 23 AM (8)](https://github.com/user-attachments/assets/8769e40b-c9dc-40c9-b6d2-716479f2787c)



grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 23 AM (9)](https://github.com/user-attachments/assets/bf6b9503-6889-4393-9d76-eb96599dae00)



cat newfile | grep -i "hello"
## OUTPUT

![WhatsApp Image 2026-01-30 at 9 21 23 AM (11)](https://github.com/user-attachments/assets/ad4bfebd-3777-47ef-8572-da0d916db8f2)



cat newfile | grep -i -c "hello"
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 23 AM (12)](https://github.com/user-attachments/assets/b7d73a57-aeac-4452-9c4d-56b37f783548)




grep -R ubuntu /etc
## OUTPUT

![WhatsApp Image 2026-01-30 at 9 21 23 AM (13)](https://github.com/user-attachments/assets/14814ba2-0fcf-4ca6-9454-55811811b79b)


grep -w -n world newfile   
## OUTPUT

![WhatsApp Image 2026-01-30 at 9 21 23 AM (14)](https://github.com/user-attachments/assets/804c9b0f-2724-4ae6-b52a-3339827d8c51)

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
![WhatsApp Image 2026-01-30 at 9 21 23 AM (15)](https://github.com/user-attachments/assets/2139e802-77c4-416b-860f-b4d8c8aa950b)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 23 AM (16)](https://github.com/user-attachments/assets/96f8744c-dcee-4271-bf58-81d7f0a6f662)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![WhatsApp Image 2026-01-30 at 9 21 23 AM (17)](https://github.com/user-attachments/assets/b77fde00-8e2a-48e6-8b4f-3fcb41c8e553)




egrep '(^hello)' newfile 
## OUTPUT

![WhatsApp Image 2026-01-30 at 9 21 23 AM (18)](https://github.com/user-attachments/assets/1d4a0c50-e248-402d-a2b0-458e11e72c00)



egrep '(world$)' newfile 
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 23 AM (19)](https://github.com/user-attachments/assets/fe97cd72-35e2-4752-8b02-ab5e0c4abf4b)



egrep '(World$)' newfile 
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 23 AM (20)](https://github.com/user-attachments/assets/8482ced4-85b1-42e7-a2c0-ba1629b715b3)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 23 AM (21)](https://github.com/user-attachments/assets/e196e831-2a31-4160-9b80-052736a8e6c9)



egrep '[1-9]' newfile 
## OUTPUT

![WhatsApp Image 2026-01-30 at 9 21 23 AM (22)](https://github.com/user-attachments/assets/149ef7ff-e7ff-49e9-8db7-800a23e27d18)


egrep 'Linux.*world' newfile 
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 23 AM (23)](https://github.com/user-attachments/assets/9e7ebbe2-2e66-47a6-801e-d5994971edac)


egrep 'Linux.*World' newfile 
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 23 AM (24)](https://github.com/user-attachments/assets/55d8bb96-bcaf-4d09-9cb6-4229da4f1d1e)


egrep l{2} newfile
## OUTPUT

![WhatsApp Image 2026-01-30 at 9 21 23 AM (26)](https://github.com/user-attachments/assets/8296267a-6767-4187-b84e-4237ee59933f)


egrep 's{1,2}' newfile
## OUTPUT 
![WhatsApp Image 2026-01-30 at 9 21 23 AM (27)](https://github.com/user-attachments/assets/12770fe4-40be-4698-9414-c8d5ef8ec912)


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

![WhatsApp Image 2026-01-30 at 9 21 23 AM (28)](https://github.com/user-attachments/assets/b1fe615a-b981-47eb-8fc5-f5b0636da3e1)


sed -n -e '$p' file23
## OUTPUT

![WhatsApp Image 2026-01-30 at 9 21 23 AM (29)](https://github.com/user-attachments/assets/2aba5544-6726-48b5-be25-3e9789039235)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM](https://github.com/user-attachments/assets/afb3c991-3580-42a3-af28-cdf70352ba9f)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (1)](https://github.com/user-attachments/assets/b4ce6816-61fa-4873-8ef5-b83c4980a05c)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (2)](https://github.com/user-attachments/assets/8df93e35-2680-4497-8849-7138af961f55)



sed -n -e '1,5p' file23
## OUTPUT

![WhatsApp Image 2026-01-30 at 9 21 24 AM (3)](https://github.com/user-attachments/assets/3bbd39bf-f62f-400b-825d-57fc88c285e2)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (4)](https://github.com/user-attachments/assets/c96400c4-e018-4169-a200-c6b84205d8a7)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (5)](https://github.com/user-attachments/assets/df41a214-943f-4253-b7a3-2304fec39d0a)



seq 10 
## OUTPUT

![WhatsApp Image 2026-01-30 at 9 21 24 AM (6)](https://github.com/user-attachments/assets/c48ecb32-4bcb-470f-a53d-a23598ca6970)


seq 10 | sed -n '4,6p'
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (7)](https://github.com/user-attachments/assets/92cfc146-a061-4316-bef3-1de284ecf951)



seq 10 | sed -n '2,~4p'
## OUTPUT

![WhatsApp Image 2026-01-30 at 9 21 24 AM (8)](https://github.com/user-attachments/assets/496835c8-4f76-43f3-8c2f-1889301a99af)



seq 3 | sed '2a hello'
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (9)](https://github.com/user-attachments/assets/b0cf5acb-9768-4e69-9ed0-b80b000544ed)



seq 2 | sed '2i hello'
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (10)](https://github.com/user-attachments/assets/0f626d5f-70ca-4e11-91c6-c1d26aac70ae)


seq 10 | sed '2,9c hello'
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (11)](https://github.com/user-attachments/assets/cbf23588-9baa-4a6f-ba19-64fc89d2eb8e)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (13)](https://github.com/user-attachments/assets/1bb24ef4-22ae-41d8-97c4-fb277679e4f1)



sed -n '2,4{s/$/*/;p}' file23
![WhatsApp Image 2026-01-30 at 9 21 24 AM (14)](https://github.com/user-attachments/assets/25ed6f21-d6a1-4cb5-81d9-36695a935129)


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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (15)](https://github.com/user-attachments/assets/b03da6ad-f0f2-4cbe-9554-ca926fc2cafa)


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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (16)](https://github.com/user-attachments/assets/ccc761cc-782f-4d37-b78d-921d38cf57c1)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (17)](https://github.com/user-attachments/assets/5cacac0c-8466-4619-b2aa-5a0f4655fbdc)

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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (18)](https://github.com/user-attachments/assets/0d92ddb6-62c1-4af6-bd65-1b38b7e204ff)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (19)](https://github.com/user-attachments/assets/85f7c162-1aea-4cd3-a4d0-4e916efc257f)



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (20)](https://github.com/user-attachments/assets/99e8a145-73ac-463e-8566-e23aeef84999)

tar -xvf backup.tar
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (21)](https://github.com/user-attachments/assets/15f53c6f-e7e7-446a-a9a8-a811b3b395e2)

gzip backup.tar

ls .gz
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (22)](https://github.com/user-attachments/assets/63f5ec77-8b96-4ee9-9d93-2e1e8fccbb34)
 
gunzip backup.tar.gz
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (28)](https://github.com/user-attachments/assets/d6f75808-3339-4a6b-8de5-fb08780eeff3)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (29)](https://github.com/user-attachments/assets/7a01bf5f-c9a1-4043-946f-87ac6d5aa83d)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (30)](https://github.com/user-attachments/assets/49e1d46e-750f-4b2f-921f-98c62d231177)


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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (31)](https://github.com/user-attachments/assets/70198a29-a076-4ea0-b1df-0bb6a2959295)

 
ls file1
## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (32)](https://github.com/user-attachments/assets/56d9cfa7-409c-4195-8db3-61d0efebbd16)

echo $?
## OUTPUT 
![WhatsApp Image 2026-01-30 at 9 21 24 AM (33)](https://github.com/user-attachments/assets/d7795271-a059-4c82-affb-f2a4c6eddbf6)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![WhatsApp Image 2026-01-30 at 9 21 24 AM (34)](https://github.com/user-attachments/assets/5b996e49-d4b3-4d3b-9d03-7ce87e8a0daa)

abcd
 
echo $?
 ## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (35)](https://github.com/user-attachments/assets/468f744a-e358-4668-a485-c3dd0cc21b37)


 
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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (37)](https://github.com/user-attachments/assets/e55eda25-a818-4c72-92bb-6d0ce3fb1ba7)



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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (38)](https://github.com/user-attachments/assets/5b03e420-c4fa-4e25-8867-9b93d36ef27c)

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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (41)](https://github.com/user-attachments/assets/1090a121-788d-49d9-b831-8a50ae0de2ad)



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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (39)](https://github.com/user-attachments/assets/82dc85c4-e82f-46b4-b2a0-cc9b500fadd9)

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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (41)](https://github.com/user-attachments/assets/b16d6432-bb24-4397-a5ad-102e5236ac35)

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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (42)](https://github.com/user-attachments/assets/9768e1c7-afa9-4e01-becb-c126f86a738c)


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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (44)](https://github.com/user-attachments/assets/367b503e-70e8-41ac-8790-bc575f3943d1)

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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (45)](https://github.com/user-attachments/assets/e0b6588d-7bc2-42ec-8286-cbc6b9b72ac7)

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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (46)](https://github.com/user-attachments/assets/cc5d436f-04c0-4838-9433-39f3a09dbba0)


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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (47)](https://github.com/user-attachments/assets/4293baf7-da57-4d97-a5cf-8d4b667d6bbc)

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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (47)](https://github.com/user-attachments/assets/9ec66653-6b6e-401d-bc06-745f48bc253b)


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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (48)](https://github.com/user-attachments/assets/e51266fb-54cd-49de-b9b1-638fb6daf6b9)

 
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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (49)](https://github.com/user-attachments/assets/22a16661-4233-43d4-a733-95ddb2c36106)

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
 ![WhatsApp Image 2026-01-30 at 9 21 24 AM (50)](https://github.com/user-attachments/assets/ef5d19e4-daa8-4759-a010-ed9461498bd7)

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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (51)](https://github.com/user-attachments/assets/f94548c3-633d-4390-a29f-9c0aa7c2f3fc)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![WhatsApp Image 2026-01-30 at 9 21 24 AM (52)](https://github.com/user-attachments/assets/d6ee51ec-6947-43fe-9028-40b555ca8798)



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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (53)](https://github.com/user-attachments/assets/06fe32cc-cb43-4fb3-8645-7bb91cb40375)

 
 ./funcex.sh 1 2
![WhatsApp Image 2026-01-30 at 9 21 24 AM (54)](https://github.com/user-attachments/assets/15dce2de-eab5-43e1-9799-19e3b7f99ca1)

 
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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (55)](https://github.com/user-attachments/assets/5a856ea0-89d8-4891-8e6f-6f887d9c3ab8)
 
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
![WhatsApp Image 2026-01-30 at 9 21 24 AM (56)](https://github.com/user-attachments/assets/ba286f45-d6e1-43a8-9f83-fa8d56cb3f62)

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
 ![WhatsApp Image 2026-01-30 at 9 21 24 AM (57)](https://github.com/user-attachments/assets/3cafd928-4882-4471-8df2-45e21d03cf80)

 
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
 ![WhatsApp Image 2026-01-30 at 9 21 24 AM (60)](https://github.com/user-attachments/assets/d608b543-3c67-4545-930f-86255dc6a0a5)

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
![WhatsApp Image 2026-01-30 at 9 21 23 AM (30)](https://github.com/user-attachments/assets/68d5fad8-73b5-4b66-ba45-452e277f4f8d)


# RESULT:
The Commands are executed successfully.
