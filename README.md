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
  The following will open the Kate GUI with a new file called "text1"
  ```
  kate text1
  ```
  We write "hello there" in the GUI and then save the file.

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

* Append 1234567890 to file text1 using echo?

  ``` bash
  echo 1234567890 >> text1
  ```
  
* Dump the contents of text1 to the terminal window?

  ``` bash
  cat text1
  ```

* Copy text1 to the directory /tmp?
  ``` bash
  cp ./text1 /tmp
  ```

* Delete text1 and text2 in one go?
  ``` bash
  rm ./text2 ./text2
  ```

* Delete the directory /home/stud/test?
  ``` bash
  rm /home/stud/test -R
  ```

* Explain how ﬁle permissions work - check the chmod and read its man page

  4 = read
  2 = write
  1 = execute

  Permissions are given to "owner", "group" and "all" as a combination of those numbers - that is 5 is "read and execute", and 6 is "read and write". "777" is "read write execute" for owner, group and all

## Program control

* Run the program Kate in the background
  ``` bash
  kate &
  ```

* Now kill the program Kate you just started
  ``` bash
  pidof kate
  ```
  will yield the PID of the process. This PID is also returned when creating the process.

  ```
  kill -9 {pid}
  ```
  replace {pid} with kate PID

* Now, write a small shell script that echos "hello world" every second. Search for bash-scripts, while-do, sleep and echo. Remember to make your shell script executable using the program chmod.

* Which chmod command?
* Shell script?
* How do you terminate it?

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

* Find the IP address of the network adapter ens33xxx

``` bash
ifconfig
```
The command returns the following output:
``` output
ens33: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.78.128  netmask 255.255.255.0  broadcast 192.168.78.255
        inet6 fe80::16ca:bed:14d5:8bbf  prefixlen 64  scopeid 0x20<link>
        ether 00:50:56:3a:36:5f  txqueuelen 1000  (Ethernet)
        RX packets 203796  bytes 259884129 (259.8 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 30760  bytes 2528912 (2.5 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
...
```
We can see the IP address is: ``192.168.78.128``.

* Explain what the ﬁle /var/log/syslog does
* Try using running less /var/log/syslog and read the manual for less. What is it good for?
* What happens when you run dmesg?
* Extending the above like this: dmesg|less, what does it do?
* Determine the CPU type by looking the directory /proc

## SSH

Try:

``` bash
ping 10.9.8.2
```

If it does not work from you virtual machine (VMware) select: Player > Removeable Devices > Netchip RNDIS/Ethernet Gadget

Attempt to ping againg once you have connected the device to the virtual machine.

``` bash
ssh root@10.9.8.2
```

``` bash
scp stud@10.9.8.1:/home/stud/hello.txt ~
```
