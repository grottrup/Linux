# Assignment 2

### 

SWT: 12, 16

``` bash
echo 12 > /sys/class/gpio/export
```

``` bash
cat /sys/class/gpio/gpio12/direction
in
```

### b

``` bash
root@raspberrypi0-wifi:~# cat /sys/class/gpio/gpio12/value     
1
```

When pressing the key:

``` bash
root@raspberrypi0-wifi:~# cat /sys/class/gpio/gpio12/value
0
```

### c

LED0 ``GPIO26``

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
