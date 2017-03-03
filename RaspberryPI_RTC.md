This is how you add an RTC to Raspberry PI

```bash
sudo nano /etc/modules 
rtc-ds1307 at the end of the file:

sudo nano /etc/rc.local

echo ds1307 0x68 > /sys/class/i2c-adapter/i2c-1/new_device
sudo hwclock -s
date
```
Just before the exit 0. Note: If you have a Rev 1 Pi, replace i2c-1 by i2c-0 above.
