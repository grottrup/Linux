# Linux
## File & Directory operations

* Display the full path of the current folder?

``` bash
pwd
```

* What does the “∼” mean in relation to a path in Unix?

It is the home dirctory of the current user

* Get a list of all ﬁles and folders in the current folder?

``` bash
ls -a
```

* Change directory to /home/stud?

``` bash
cd ~
```

* Create a directory /home/stud/test?

``` bash
mkdir ~/test
```

* Change directory to the subdirectory /home/stud/test?

``` bash
cd test
```

* Create a ﬁle text1 containing "hello there" using Kate?
```
kate text1
```
write "hello there" in the GUI and then save the file

* Install Kate if it is not present? (Or Atom or Code if you prefer)

``` bash
sudo apt install kate
```

``` bash
sudo snap install code --classic
```

* Create a ﬁle text2 containing "hello there" using echo?

``` bash
echo "hello there" > text2
```

* Append 1234567890 to file text1 using echo? **(Todo)**
* Dump the contents of text1 to the terminal window?

``` bash
cat text1
```

* Copy text1 to the directory /tmp? **(Todo)**
* Delete text1 and text2 in one go? **(Todo)**
* Delete the directory /home/stud/test? **(Todo)**

Explain how ﬁle permissions work - check the chmod and read its man page **(Todo)**

## Program control

* Run the program Kate in the background **(Todo)**
* Now kill the program Kate you just started **(Todo)**

Now, write a small shell script that echos "hello world" every second. Search for bash-scripts, while-do, sleep and echo. Remember to make your shell script executable using the program chmod. **(Todo)**

* Which chmod command? **(Todo)**
* Shell script? **(Todo)**
* How do you terminate it? **(Todo)**

## Acquiring system information

* Get a list of the currently running processes (programs)

For user processes:??????????

``` bash
ps
```

For every process:

``` bash
ps -e
```

* Display the current date and time in the terminal

``` bash
date
```

* Find the IP address of the network adapter ens33xxx **(Todo)**
* Explain what the ﬁle /var/log/syslog does **(Todo)**
* Try using running less /var/log/syslog and read the manual for less. What is it good for? **(Todo)**
* What happens when you run dmesg? **(Todo)**
* Extending the above like this: dmesg|less, what does it do? **(Todo)**
* Determine the CPU type by looking the directory /proc **(Todo)**

## SSH

``` bash
ping 10.9.8.2
```
``` bash
ssh root@10.9.8.2
```

``` bash
scp stud@10.9.8.1:/home/stud/hello.txt ~
```
