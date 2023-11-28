# kkhmf-ili9341-tft

# compile & deploy

In PC
~~~
cd dts
dtc -O dtb -o kkhmf-ili9341-tft.dtbo kkhmf-ili9341-tft.dts
scp kkhmf-ili9341-tft.dtbo rpi@raspberrypi.local:
~~~

In rpi4
~~~
cp kkhmf-ili9341-tft.dtbo /boot/overlay
sync
~~~

/boot/config.txt
~~~
dtparam=spi=on
dtoverlay=kkhmf-ili9341-tft
~~~

# test 

fbtest

~~~
$ git clone https://git.kernel.org/pub/scm/linux/kernel/git/geert/fbtest.git
$ cd fbtest
$ make
$ ./fbtest
~~~

evtest
~~~
sudo apt-get install -y evtest
~~~
