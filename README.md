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
## Name:Meenakshi.R
## Register No:212224220062
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

<img width="165" height="86" alt="309798830-645747f6-840a-4fb5-9bb8-3d37985808e1" src="https://github.com/user-attachments/assets/29ed69b4-b077-4e42-981b-5f3318c9da55" />

cat < file2
## OUTPUT

<img width="157" height="104" alt="309799356-4680c410-0f1a-417d-9f0d-05e417dff105" src="https://github.com/user-attachments/assets/29a8bb0e-7d0c-48e9-a15a-828009171914" />



# Comparing Files
cmp file1 file2
## OUTPUT

<img width="271" height="36" alt="309799683-b72ea53a-f252-420f-b008-c1db50733c87" src="https://github.com/user-attachments/assets/a6f0de45-88c3-4a07-bfcc-3f4b2b9c56ec" />


comm file1 file2
 ## OUTPUT

 <img width="294" height="181" alt="309800849-9d8206de-18fe-42e7-98c7-f58a03d1e027" src="https://github.com/user-attachments/assets/0a56ebaa-65de-4a28-b31d-2402481e9860" />


diff file1 file2
## OUTPUT

<img width="200" height="171" alt="309800157-9db3fd92-ee1d-45f1-81b7-2421566f2f4a" src="https://github.com/user-attachments/assets/b81fb215-5907-49fb-9e3f-698c1e612b51" />


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


<img width="199" height="75" alt="309801929-b05fb00f-680e-478f-bf30-40e73ed3f8fc" src="https://github.com/user-attachments/assets/8c0c09cb-a06a-4b9a-a5a9-f50b17193422" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="220" height="68" alt="309802390-9b1db5ba-2294-4c27-93e3-04529c484132" src="https://github.com/user-attachments/assets/7b868abd-5f87-4ce0-abd7-60bb03670379" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="201" height="95" alt="309802553-ac5c3093-ce26-4a44-8342-2861d83fe00c" src="https://github.com/user-attachments/assets/3d435e57-398c-4e5e-b7b2-60963d8a61a6" />


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

<img width="282" height="38" alt="309804197-c9dcc002-ec57-4d2a-ac12-b2118670b418" src="https://github.com/user-attachments/assets/a42dd651-7d62-41e0-b2ac-c82a2a15a397" />

grep hello newfile 
## OUTPUT

<img width="190" height="35" alt="309803542-1ba59f65-d89a-443c-b63e-658844690510" src="https://github.com/user-attachments/assets/b07d0ebe-4f91-4be0-9241-d8057b5b3aeb" />

grep -v hello newfile 
## OUTPUT

<img width="195" height="35" alt="309804420-7898aa37-f171-4dd3-b9bf-4821a7c66366" src="https://github.com/user-attachments/assets/d1a86367-0e43-4d25-99e8-6412b82c73c6" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="286" height="55" alt="309804644-b34be529-da32-4875-ada4-5403c4b2b219" src="https://github.com/user-attachments/assets/e3d76e0d-1671-444e-a6a4-965d0b97a76b" />

cat newfile | grep -i -c "hello"
## OUTPUT

<img width="263" height="36" alt="309804896-b68bbe48-76d8-4261-aea9-5b3525862b73" src="https://github.com/user-attachments/assets/71301c33-64be-445c-9584-e46f540df6c1" />

grep -R ubuntu /etc
## OUTPUT

<img width="1289" height="446" alt="309805946-c7641628-681a-431e-a85d-f9606f4a5cf5" src="https://github.com/user-attachments/assets/29604df2-6129-45cb-bb0c-949123c88dd7" />


grep -w -n world newfile   
## OUTPUT

<img width="217" height="50" alt="309806230-ab89cc80-61df-49c7-b155-4a5e5172bb58" src="https://github.com/user-attachments/assets/8b264184-b40f-4891-8201-abbf8a9b7af5" />


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

<img width="321" height="58" alt="309807165-3fb6eac9-fb4a-4396-9418-c277da0ac7af" src="https://github.com/user-attachments/assets/6ee6e90f-980d-4eaf-ab4b-fd2a4a0e3692" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="258" height="73" alt="309807392-15faa397-b760-4e38-88c5-46df8d1bdb60" src="https://github.com/user-attachments/assets/c4981e84-0780-48f5-b8e3-c4422afe4dbe" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="320" height="78" alt="309807587-cb5df577-6ca4-4fb2-a5b2-a1bbfc9342ff" src="https://github.com/user-attachments/assets/f8f806de-b769-4bdb-94ff-85a78e328558" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="256" height="73" alt="309807775-84e6db99-923d-4dcb-9d2f-f759f1d23029" src="https://github.com/user-attachments/assets/45db32d7-46e2-4b7e-a0d8-5e1ba2bfe0b7" />

egrep '(world$)' newfile 
## OUTPUT

<img width="219" height="67" alt="309808081-3e4a7354-30a8-4a78-9ba7-ef3d7b9205cc" src="https://github.com/user-attachments/assets/0ee4e199-c3aa-4b04-9ccf-6249b511cbbb" />


egrep '(World$)' newfile 
## OUTPUT
<img width="234" height="58" alt="309811412-73eb50dd-a4e7-4231-93fd-3043957f5bb6" src="https://github.com/user-attachments/assets/cfac0d9d-2fbb-4866-b5b0-c20365a55d80" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="249" height="68" alt="309811661-10d9f5b0-41c6-4871-8acb-7c1bbfbefaaa" src="https://github.com/user-attachments/assets/8b676f99-d431-4b05-b05f-14a60f48858f" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="242" height="35" alt="309813236-56fd1f75-45fe-46f6-8ed2-f25c8c712aec" src="https://github.com/user-attachments/assets/d136a4d2-78cb-423c-8d24-174395ab0c33" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="262" height="33" alt="309813430-7d6419cf-634f-4106-9a64-86fb2f8098c3" src="https://github.com/user-attachments/assets/fe13de86-b9f7-4c6f-b5fe-a733d5ad6e9d" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="271" height="55" alt="309813792-1128e562-d671-4878-a83c-49a308d4f983" src="https://github.com/user-attachments/assets/7209f603-d580-483f-9e65-781c4e099cda" />

egrep l{2} newfile
## OUTPUT

<img width="234" height="67" alt="309814070-da8d070f-5f44-421c-b63e-b08b08021b2d" src="https://github.com/user-attachments/assets/d995c814-67f2-4854-b4ff-b6b24cb21975" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="304" height="78" alt="309814327-c79a5769-68c8-4842-87e9-d9799398d1dc" src="https://github.com/user-attachments/assets/2699c13a-62ae-4ea3-9583-365cbe1d641e" />

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

<img width="226" height="51" alt="309814693-d023edb3-6837-4065-98e9-08bb8b5d4360" src="https://github.com/user-attachments/assets/5dd5ad8b-57cb-41b3-8046-20b7aa3c49c2" />


sed -n -e '$p' file23
## OUTPUT

<img width="226" height="51" alt="309814693-d023edb3-6837-4065-98e9-08bb8b5d4360-1" src="https://github.com/user-attachments/assets/1cb3c589-8fee-4004-b2a8-1e7df039e080" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="291" height="170" alt="309815343-03ea1332-8ae5-4e5b-9f27-5f150319a13b" src="https://github.com/user-attachments/assets/c38af860-4907-43c0-aa09-e360f84225d9" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="301" height="173" alt="309815611-54e0938a-b87e-4a52-a6d8-1d33b644ef58" src="https://github.com/user-attachments/assets/8b10294d-c83a-4586-9017-bb93726fdf12" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="315" height="179" alt="309815956-f4539868-4ccb-480e-a828-de27371cc413" src="https://github.com/user-attachments/assets/6e397738-509c-48d5-ab6a-73213ec9a046" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="297" height="119" alt="309816318-61c2937f-7b06-4bae-828a-7e00818b5287" src="https://github.com/user-attachments/assets/446c50e1-3d37-4c9e-8b49-5dd9eaee6b55" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="304" height="64" alt="309819642-07aa75ef-5b1e-4d5b-bfe5-7d36cb65c8d7" src="https://github.com/user-attachments/assets/d515e96b-9dcd-4824-b9ac-26883cf7956d" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="291" height="69" alt="309819759-b3664d94-dc31-448c-88b1-e74cd741c96b" src="https://github.com/user-attachments/assets/4d2c218d-646e-4b6f-b4ab-8199fef9203e" />


seq 10 
## OUTPUT

<img width="266" height="205" alt="309819968-b51046e0-51df-4a04-97a3-9aff3b3929fd" src="https://github.com/user-attachments/assets/a91de0d3-f0be-4b77-b103-903febf3418b" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="279" height="87" alt="309820170-4ed9f3b2-3d9a-4859-a477-9c4d47247f26" src="https://github.com/user-attachments/assets/d8fb3ff5-0753-4cbe-a5a4-a6754d338a7d" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="278" height="84" alt="309820615-a910466b-be1c-4335-8842-201a475247b6" src="https://github.com/user-attachments/assets/6566708e-d6d1-49fc-a338-8904978e8fa0" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="291" height="102" alt="309820771-40491877-b232-4596-96a2-c3d9955510e8" src="https://github.com/user-attachments/assets/bf578470-c530-4651-94ec-744925e0e68f" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="246" height="86" alt="309821238-c0cd675e-bff0-4f16-a406-081556b997ad" src="https://github.com/user-attachments/assets/3f2b1239-7e67-49f8-abd8-5e110b4ebb34" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="267" height="85" alt="309821431-0867c436-fe08-4955-b19f-d73264f8008b" src="https://github.com/user-attachments/assets/abe0f42a-b4d3-4fae-8007-5e7c0a625c1c" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="290" height="91" alt="309821572-97a3d875-4b77-48e6-bba7-a65eedd77df3" src="https://github.com/user-attachments/assets/3ecb1065-c754-4d1a-8113-6cad63d0022d" />


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

<img width="238" height="114" alt="309822352-ef7e2f21-aca3-4acd-818a-4f55a6cc180b" src="https://github.com/user-attachments/assets/f00f9a5b-165a-4dfe-a815-c65aaac6473c" />

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

<img width="245" height="117" alt="309823420-1f2963c8-35ed-4d50-9053-02ce2a88be06" src="https://github.com/user-attachments/assets/27437620-293b-450f-83ad-31b5b04804ee" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
<img width="311" height="166" alt="309823860-dbf6ba03-73d0-4af8-8dc3-0d50d2d6afb4" src="https://github.com/user-attachments/assets/bf534153-8d16-4685-8cee-e5afc3f08ff3" />

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

<img width="314" height="92" alt="309824719-0729a6c7-8b70-4a6e-93dd-369f6a699821" src="https://github.com/user-attachments/assets/55b56aa3-f542-4eb6-805e-9d2c055621e0" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="328" height="92" alt="309824984-36ecee6f-5496-4b22-909a-5fe77534e6dc" src="https://github.com/user-attachments/assets/a46e31f7-bb2f-4710-bdb5-35e02d7ee4f9" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="230" height="208" alt="309825316-81b64612-f73a-4d36-8b08-a1615ab5e326" src="https://github.com/user-attachments/assets/c9080677-bc17-4f95-8825-edd0532109a9" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="553" height="203" alt="309825519-eb10b39d-0ce2-4e71-ab67-37fc7cc9d18b" src="https://github.com/user-attachments/assets/90a446b5-544e-466a-8090-2b42a82da931" />

tar -xvf backup.tar
## OUTPUT

<img width="219" height="208" alt="309826053-1b4ddf40-3c5d-45e7-ae2b-914819b4c2ec" src="https://github.com/user-attachments/assets/004f23b0-6df5-4e4b-8d2c-f69eb6480f1a" />

gzip backup.tar

ls .gz
## OUTPUT

<img width="125" height="57" alt="309827418-f9334fa8-a252-415c-b056-c1f9b5d80b38" src="https://github.com/user-attachments/assets/b87cdc02-db57-4711-9f5a-d1eed4f2da8d" />

gunzip backup.tar.gz
## OUTPUT

<img width="123" height="54" alt="309828162-5f0b0094-2c2c-40f3-884f-0c0dcecc24f1" src="https://github.com/user-attachments/assets/3f2874e7-8314-4fc4-9669-b7bf780de601" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="376" height="110" alt="309830670-c7f6eac0-d1a0-4703-9a07-2d631edd84d7" src="https://github.com/user-attachments/assets/63b0a418-58eb-4862-ab62-0ff5550e863f" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="260" height="85" alt="309831247-18cbf086-541c-4bb1-92ab-c814bdf8c142" src="https://github.com/user-attachments/assets/95df32a8-6357-4eb0-b107-57430b551419" />

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

<img width="460" height="362" alt="309832793-888cca6e-adb3-4897-99a7-fd743ee6f1bd" src="https://github.com/user-attachments/assets/bb1bb7a2-685c-47a2-aefd-0df2d9a3c953" />

ls file1
## OUTPUT

<img width="122" height="56" alt="309833097-8aa7a308-1319-4bfe-b9c2-7929272e63cc" src="https://github.com/user-attachments/assets/fd2d3c95-2ca3-4280-8235-5057441f6708" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT

<img width="136" height="55" alt="309833203-f0d7cbbc-d1eb-42b7-830b-91c7bc5797f4" src="https://github.com/user-attachments/assets/75511be8-4c57-4933-8963-ca672b69d528" />

 
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

<img width="265" height="192" alt="309833825-35a3a9c0-5224-4e0f-bae9-6c603032ec8e" src="https://github.com/user-attachments/assets/c17a9eef-dc67-4b26-b038-869df03d1c87" />

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

<img width="470" height="125" alt="309836204-d95b622a-155f-4e82-a895-818b862dbca1" src="https://github.com/user-attachments/assets/629c18eb-e8d0-4f8e-bc00-b831f6fa911f" />


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

<img width="455" height="106" alt="309836560-031d4ce7-6bf5-4cf0-9ef6-3c6fad1b8752" src="https://github.com/user-attachments/assets/4ded6c6a-1d50-437f-9967-f43502986e1e" />

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

<img width="448" height="122" alt="309837253-b67da7ca-c91d-4a9f-8d63-c24b01a28434" src="https://github.com/user-attachments/assets/da07f3fd-608f-4ee6-9558-118417bd7af4" />

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

<img width="508" height="85" alt="309837620-a955d321-158d-46a5-a932-dbe21449c991" src="https://github.com/user-attachments/assets/afa27180-14b9-4802-b40d-da1c3d411324" />

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

<img width="451" height="89" alt="309839617-24882ffa-4666-48a8-80b0-92c170da5e60" src="https://github.com/user-attachments/assets/1b34e417-1780-4251-9173-6d1e9e49fc7e" />

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
## Output

<img width="319" height="75" alt="309840177-fd8b7441-e413-4c34-b35e-72d6b8e953bd" src="https://github.com/user-attachments/assets/3378aa51-4627-4c41-b79a-e68c2871eafb" />

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
## Output

<img width="254" height="229" alt="309840585-e4f9b365-56ff-4898-b0fd-44843212470a" src="https://github.com/user-attachments/assets/4bb92104-4c33-4d46-b2d8-e8cff7b93d34" />

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
## Output

<img width="258" height="120" alt="309840951-22431f68-6b65-49ec-9287-eeb6d31792a4" src="https://github.com/user-attachments/assets/b79f900d-334b-45fb-ab5c-645eba3cddae" />

 
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
## Output

<img width="214" height="151" alt="309841701-8766aba0-572e-4a9b-bd39-03c7e64820b1" src="https://github.com/user-attachments/assets/0a5d85b6-4337-42ef-bae2-75b8629cd118" />

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
## Output

<img width="275" height="106" alt="309842258-169751ae-053b-424e-b0ab-63ef3308d633" src="https://github.com/user-attachments/assets/15b4be61-1cd6-466b-8d33-e8f3f3c06470" />

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
## Output

 <img width="249" height="159" alt="309842703-20318e60-4a59-472f-ac43-2f3fb6dcd9b9" src="https://github.com/user-attachments/assets/1f35eb34-5e3b-4c7b-a6ba-9ab24a602089" />

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

<img width="339" height="284" alt="309843870-1ee1082b-0af5-42d2-8088-78ba28ca6c20" src="https://github.com/user-attachments/assets/3e6af088-7f24-4691-ba81-ca06d3b0f2a5" />

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
<img width="255" height="145" alt="309844476-18486ab6-4411-45e3-8f9f-fa86c28172a5" src="https://github.com/user-attachments/assets/54eca728-3c6c-4f96-a6be-af3de0e437de" />

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
<img width="243" height="129" alt="309844741-841f1a13-e515-4529-b171-cd063a871600" src="https://github.com/user-attachments/assets/9979887f-b7cb-42f3-95a5-b23cfc722dcb" />

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

 <img width="283" height="250" alt="309845143-1bdc895e-f05e-4992-9c84-b482adc312d0" src="https://github.com/user-attachments/assets/3041fae6-3476-4b72-bd84-aede2583806d" />

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
<img width="389" height="128" alt="309847528-b8396871-2ea9-4236-8a0b-f7ca315c2d98" src="https://github.com/user-attachments/assets/9514bb85-57dd-41c1-9ebe-6f5405ae8094" />

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
 <img width="352" height="141" alt="309847970-2f5a8645-be73-45eb-840b-8a9d23274fb6" src="https://github.com/user-attachments/assets/ab13f84c-875f-40a6-9fb0-d06df8a6c5fd" />

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

<img width="338" height="95" alt="309851345-b459d5c6-e132-4bc5-845d-ed2316ca8f75" src="https://github.com/user-attachments/assets/6be5753e-fe32-4716-a42f-ccc25c748045" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="196" height="106" alt="309851670-f8502838-935e-4fda-9fe1-502e60e42c68" src="https://github.com/user-attachments/assets/1071ffa0-1198-43fa-b8c9-e5460a47524d" />

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

 <img width="229" height="121" alt="309852244-62cd062e-c179-4e5a-9ab8-9a83f6b78032" src="https://github.com/user-attachments/assets/b291ae8d-77a0-4c7d-a09d-c8cedb459f05" />

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
$ ./argshift.sh 1 2 3
 
 <img width="282" height="139" alt="309853113-e82552ac-1446-4b63-91a2-fe9947fa3ca3" src="https://github.com/user-attachments/assets/339fd84a-1f7d-4df3-a598-630ff4132969" />

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

<img width="240" height="118" alt="309853667-c104a58c-d3d6-4d6b-930b-d7779001e0ea" src="https://github.com/user-attachments/assets/167edd5a-41e6-413d-9d76-ff380476d513" />

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
 
 <img width="295" height="307" alt="309853957-be6b3831-7903-4684-a5ad-4969e49f766a-1" src="https://github.com/user-attachments/assets/278ed3c7-6341-4e7a-8e5b-b0205def8938" />

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

 <img width="290" height="256" alt="309854432-6cc7231e-1fe4-4a75-8d76-712cf7246e4a" src="https://github.com/user-attachments/assets/b732e977-f36e-46d1-b88a-c97e1149fa06" />

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

<img width="250" height="103" alt="309855037-9d97b191-3f17-43eb-8883-e773907c2eea" src="https://github.com/user-attachments/assets/21ac0381-ffc7-41fa-8544-a61d64c07551" />

# RESULT:
The Commands are executed successfully.
