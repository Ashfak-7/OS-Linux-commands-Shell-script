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


<img width="435" height="147" alt="image" src="https://github.com/user-attachments/assets/2ddb32ca-2290-4a95-97ff-5b1226bbf9fc" />




cat < file2
## OUTPUT

<img width="495" height="176" alt="image" src="https://github.com/user-attachments/assets/ffd9c307-0d19-40d6-bec5-c906b30e6aff" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="517" height="75" alt="image" src="https://github.com/user-attachments/assets/d4db9f1a-5118-444e-aacc-1a0bb9cf88a7" />


 
comm file1 file2
 ## OUTPUT

<img width="490" height="222" alt="image" src="https://github.com/user-attachments/assets/38e7a055-ba90-4904-a808-83962063154f" />


 
diff file1 file2
## OUTPUT

<img width="472" height="272" alt="image" src="https://github.com/user-attachments/assets/3f20b7e9-8c83-4244-9262-6b5d86d8b5e4" />



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

<img width="417" height="96" alt="image" src="https://github.com/user-attachments/assets/eed8256d-7515-48bf-8d37-521201450560" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="432" height="122" alt="image" src="https://github.com/user-attachments/assets/2441bd81-4e59-4641-8ae5-8319299f9f74" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="415" height="130" alt="image" src="https://github.com/user-attachments/assets/9fe0d89b-ca22-4f19-b070-364b0631cf07" />


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

<img width="427" height="75" alt="image" src="https://github.com/user-attachments/assets/de80b186-5a2a-44a3-a94e-cb53645385a0" />


grep hello newfile 
## OUTPUT

<img width="447" height="85" alt="image" src="https://github.com/user-attachments/assets/ad628369-74a9-469d-9e8c-78c870bd00db" />



grep -v hello newfile 
## OUTPUT

<img width="427" height="82" alt="image" src="https://github.com/user-attachments/assets/30bc8b53-4be3-44ee-abc9-cfb8af298faa" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="437" height="111" alt="image" src="https://github.com/user-attachments/assets/f0ca4ebf-415c-4785-b349-3f39061c0a05" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="450" height="82" alt="image" src="https://github.com/user-attachments/assets/c158c4d6-9545-42c4-ba3b-b6bc360f06b6" />



grep -R ubuntu /etc
## OUTPUT

<img width="717" height="430" alt="image" src="https://github.com/user-attachments/assets/80a23fe6-449b-4eff-87c1-b11faf4db913" />


grep -w -n world newfile   
## OUTPUT

<img width="472" height="110" alt="image" src="https://github.com/user-attachments/assets/fa92dd67-35c9-4e9b-b509-595c27a0e80d" />


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

<img width="460" height="102" alt="image" src="https://github.com/user-attachments/assets/0712663e-4b8e-48dd-9e27-63c79bd9cd93" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="442" height="105" alt="image" src="https://github.com/user-attachments/assets/23fc059a-06b6-4d35-a92c-61d65c298caf" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="455" height="105" alt="image" src="https://github.com/user-attachments/assets/ad3a7d3d-441f-49ec-8bb5-23ef6e87fdb9" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="442" height="82" alt="image" src="https://github.com/user-attachments/assets/5317a317-99cb-49b4-b162-16a624a970f8" />


egrep '(world$)' newfile 
## OUTPUT

<img width="442" height="107" alt="image" src="https://github.com/user-attachments/assets/d51dad8f-09b1-4bf7-9986-153149f1f3c7" />


egrep '(World$)' newfile 
## OUTPUT

<img width="437" height="85" alt="image" src="https://github.com/user-attachments/assets/2ca3d585-a863-4897-a9c2-e4c35c648490" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="480" height="127" alt="image" src="https://github.com/user-attachments/assets/09ca8905-b62f-4a85-ab7d-c0a291f24340" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="440" height="80" alt="image" src="https://github.com/user-attachments/assets/6118413a-79ac-4672-a77c-da5f234a2355" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="567" height="75" alt="image" src="https://github.com/user-attachments/assets/388ff1ce-fa87-4b5a-be55-ae22e726de2e" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="455" height="77" alt="image" src="https://github.com/user-attachments/assets/1b617735-8f0f-4e7a-b885-52cc50ac4da9" />


egrep l{2} newfile
## OUTPUT

<img width="422" height="102" alt="image" src="https://github.com/user-attachments/assets/a43f6f56-ff17-4694-9653-990eac453f9a" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="440" height="127" alt="image" src="https://github.com/user-attachments/assets/9ec2cd81-c92a-4aa8-a5cb-3cfaba9b0cd2" />


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

<img width="462" height="82" alt="image" src="https://github.com/user-attachments/assets/b4e02e94-fda2-4d1f-a55d-766114ca2f93" />


sed -n -e '$p' file23
## OUTPUT

<img width="432" height="80" alt="image" src="https://github.com/user-attachments/assets/b3e0ef7e-b3be-4b5a-a091-11f795b93843" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="450" height="252" alt="image" src="https://github.com/user-attachments/assets/50ea5b6b-25ab-4b22-92df-4887a9f738a6" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="452" height="252" alt="image" src="https://github.com/user-attachments/assets/c0e29af5-4361-4781-8364-95dc93a0fe61" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="462" height="257" alt="image" src="https://github.com/user-attachments/assets/0f9f0d6a-092d-433e-9485-e1c3052451af" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="462" height="175" alt="image" src="https://github.com/user-attachments/assets/f9666e18-05c4-4008-9a75-8410cfd7e7fd" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="472" height="135" alt="image" src="https://github.com/user-attachments/assets/4af35d80-e8de-457f-805f-6e83a084dd04" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="445" height="102" alt="image" src="https://github.com/user-attachments/assets/f12277cd-0c20-4ffa-8f70-6e31816a5dc2" />


seq 10 
## OUTPUT

<img width="427" height="306" alt="image" src="https://github.com/user-attachments/assets/01ae2743-e1be-4bac-8c39-384807068d5a" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="442" height="122" alt="image" src="https://github.com/user-attachments/assets/c42d1cdf-dccf-4493-bcfa-dbc39224fbab" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="417" height="127" alt="image" src="https://github.com/user-attachments/assets/02ebd31c-a9da-4d97-81f9-288aded3f783" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="482" height="157" alt="image" src="https://github.com/user-attachments/assets/95a2c147-090f-4751-9a5f-f600b48d9646" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="452" height="130" alt="image" src="https://github.com/user-attachments/assets/5b909658-83c9-4c39-97a1-8ca4ed2b8ad2" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="452" height="120" alt="image" src="https://github.com/user-attachments/assets/a0457b35-8053-40d7-8e53-51c35aade902" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="447" height="130" alt="image" src="https://github.com/user-attachments/assets/6a09d31c-b5d6-4e5c-a4c0-448a44b85329" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="472" height="132" alt="image" src="https://github.com/user-attachments/assets/310eccbb-e512-4fb8-b738-a5dda976e67e" />


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

<img width="490" height="181" alt="image" src="https://github.com/user-attachments/assets/cafac22a-33e4-4874-b811-a69663a42089" />


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

<img width="447" height="177" alt="image" src="https://github.com/user-attachments/assets/d478104e-91fb-497b-93c6-83498d261a84" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="562" height="257" alt="image" src="https://github.com/user-attachments/assets/de4cf754-2fe5-4594-904d-0b53a7e86fd5" />


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

<img width="480" height="127" alt="image" src="https://github.com/user-attachments/assets/6afe6246-e5bb-4b9d-b482-48e9684687b5" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="520" height="127" alt="image" src="https://github.com/user-attachments/assets/8f3ad518-a3f1-4244-8178-d425ac6dc465" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="455" height="245" alt="image" src="https://github.com/user-attachments/assets/ea20aa1f-55c0-4e67-a105-17e2d221ab5e" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="635" height="261" alt="image" src="https://github.com/user-attachments/assets/7b5b5c8a-a8a1-4064-af80-b628f72ab569" />


tar -xvf backup.tar
## OUTPUT

<img width="547" height="255" alt="image" src="https://github.com/user-attachments/assets/87c0d841-794a-48b1-ada6-268e83151edc" />


gzip backup.tar

ls .gz
## OUTPUT

<img width="572" height="80" alt="image" src="https://github.com/user-attachments/assets/5ffb06ab-2bbd-4fb7-a490-8e5d4cf05aa5" />

 
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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="512" height="125" alt="image" src="https://github.com/user-attachments/assets/1c30bed3-0f47-4641-a4b8-5d1d6d4b1eb7" />


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

<img width="670" height="407" alt="image" src="https://github.com/user-attachments/assets/7d146db1-673e-4afe-a965-e78b4cfef9e5" />

 
ls file1
## OUTPUT


<img width="490" height="97" alt="image" src="https://github.com/user-attachments/assets/41e6c55e-54da-4f26-9dfb-aac3299b29e9" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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

<img width="560" height="82" alt="image" src="https://github.com/user-attachments/assets/7c6fe1f0-8411-4905-bd69-d4db32cdbc1f" />


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

<img width="592" height="85" alt="image" src="https://github.com/user-attachments/assets/5a231af2-e3fe-4a71-adf3-09e850d22d21" />


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

<img width="567" height="142" alt="image" src="https://github.com/user-attachments/assets/1101688f-d44a-4e83-b7bf-d41727613032" />


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

<img width="537" height="100" alt="image" src="https://github.com/user-attachments/assets/61339f6b-f275-4958-a582-de6624fae223" />


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

<img width="567" height="142" alt="image" src="https://github.com/user-attachments/assets/1101688f-d44a-4e83-b7bf-d41727613032" />


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

<img width="545" height="85" alt="image" src="https://github.com/user-attachments/assets/09185495-790c-4982-a8d9-98fd653a1a41" />


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

<img width="545" height="85" alt="image" src="https://github.com/user-attachments/assets/09185495-790c-4982-a8d9-98fd653a1a41" />


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

<img width="545" height="85" alt="image" src="https://github.com/user-attachments/assets/09185495-790c-4982-a8d9-98fd653a1a41" />

 
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

 <img width="525" height="307" alt="image" src="https://github.com/user-attachments/assets/a2e03542-a2e2-4856-b227-fea43ebdfe68" />

 
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

 <img width="525" height="307" alt="image" src="https://github.com/user-attachments/assets/10eb97b3-2ba4-4709-b2cc-1c57cf5555bf" />

 
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

<img width="525" height="307" alt="image" src="https://github.com/user-attachments/assets/55173ef9-936a-4461-a1fe-84a0efb7f215" />

 
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

<img width="525" height="307" alt="image" src="https://github.com/user-attachments/assets/55173ef9-936a-4461-a1fe-84a0efb7f215" />


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

<img width="562" height="227" alt="image" src="https://github.com/user-attachments/assets/676b0046-9697-4f7c-a2a9-0a64ac373266" />


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

<img width="522" height="186" alt="image" src="https://github.com/user-attachments/assets/7d28c972-f652-487a-bc5f-53e8bf1d2e0b" />


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

<img width="522" height="186" alt="image" src="https://github.com/user-attachments/assets/3710537c-c2ac-4a9d-9913-086cc4a771d0" />


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


 <img width="522" height="186" alt="image" src="https://github.com/user-attachments/assets/f9ec9b4c-2af0-4df0-9fad-3cc6954e6378" />

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

<img width="740" height="132" alt="image" src="https://github.com/user-attachments/assets/e1211e0c-4987-4f68-ac8a-74c7bb4d2f59" />

 
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

<img width="740" height="132" alt="image" src="https://github.com/user-attachments/assets/7027960c-562e-452f-8483-f4378697b817" />

 
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

<img width="527" height="102" alt="image" src="https://github.com/user-attachments/assets/c577e2d5-eccf-4a9b-92d5-aa8ccf3a930e" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="527" height="102" alt="image" src="https://github.com/user-attachments/assets/cc465330-cc7a-42ab-9350-16e9c80c7a03" />


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
