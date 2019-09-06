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
