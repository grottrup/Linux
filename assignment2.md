# Assignment 2

### 

### a) Setup and check fHAT switch

SWT: ``GPIO12``, ``GPIO16``

``` bash
echo 12 > /sys/class/gpio/export
```

``` bash
cat /sys/class/gpio/gpio12/direction
in
```

### b) Test clicking the switch

``` bash
root@raspberrypi0-wifi:~# cat /sys/class/gpio/gpio12/value     
1
```

When pressing the key:

``` bash
root@raspberrypi0-wifi:~# cat /sys/class/gpio/gpio12/value
0
```

### c) Setup LED as output

LED0: ``GPIO26``

``` bash
echo 26 > /sys/class/gpio/export
```

``` bash
cat /sys/class/gpio/gpio26/direction
in
```

To change this to out do the following:

``` bash
echo out > /sys/class/gpio/gpio26/direction
```

``` bash
cat /sys/class/gpio/gpio26/direction
out
```

To make the LED light up run:

``` bash
echo 1 > /sys/class/gpio/gpio26/value
```

### d) Write C blinker program

idk some headers

``` c
#include <unistd.h>
#include <stdio.h>
#include <fcntl.h>
#include <errno.h>
#include <string.h>
#include <time.h>

int main(int argc, char *argv[])
{
  int fd, num_wr;
  
  char buffer[] ="1";
  char buffer2[] = "0";
  fd=open("/sys/class/gpio/gpio26/value", O_RDWR | O_CREAT, S_IRUSR|S_IWUSR);
  
    while(1)
    {
      num_wr=write(fd, buffer, 1);
      
      sleep(1);
      
      num_wr=write(fd, buffer2, 1);

      sleep(1);
    }
}

```
Create the exe file on the virtual machine:

``` bash
arm-rpizw-gcc -o ledblink ledblink.c
```

Copy the exe file to the Raspberry Pi:

``` bash
scp stud@10.9.8.1:/home/stud/Desktop/ledblink ~
```

Run it:
``` bash
./ledblink
```


