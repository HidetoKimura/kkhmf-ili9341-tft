# kkhmf-ili9341-tft

# compile & deploy

In rpi4
~~~
# dtc -o dtb kkhmf-ili9341-tft.dtbo kkhmf-ili9341-tft.dts
# cp kkhmf-ili9341-tft.dtbo /boot/overlay
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
