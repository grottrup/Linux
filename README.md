# Linux
## File & Directory operations

* Display the full path of the current folder?
```
pwd
```
* What does the “∼” mean in relation to a path in Unix?
* Get a list of all ﬁles and folders in the current folder?
* Change directory to /home/stud?
* Create a directory /home/stud/test?
* Change directory to the subdirectory /home/stud/test?
* Create a ﬁle text1 containing "hello there" using Kate?
* Install Kate if it is not present? (Or Atom if you prefer)
* Create a ﬁle text2 containing "hello there" using echo?
* Append 1234567890 to file text1 using echo?
* Dump the contents of text1 to the terminal window?
* Copy text1 to the directory /tmp?
* Delete text1 and text2 in one go?
* Delete the directory /home/stud/test?

Explain how ﬁle permissions work - check the chmod and read its man page

## Program control

* Run the program Kate in the background
* Now kill the program Kate you just started

Now, write a small shell script that echos "hello world" every second. Search for bash-scripts, while-do, sleep and echo. Remember to make your shell script executable using the program chmod.

* Which chmod command?
* Shell script?
* How do you terminate it?

## Acquiring system information

* Get a list of the currently running processes (programs)
* Display the current date and time in the terminal
* Find the IP address of the network adapter ens33xxx
* Explain what the ﬁle /var/log/syslog does
* Try using running less /var/log/syslog and read the manual for less. What is it good for?
* What happens when you run dmesg?
* Extending the above like this: dmesg|less, what does it do?
* Determine the CPU type by looking the directory /proc
