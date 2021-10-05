
Python library to read the DHT series of humidity and temperature sensors on a
Raspberry Pi or Beaglebone Black.

Designed specifically to work with the Adafruit DHT series sensors ---->
https://www.adafruit.com/products/385

Currently the library is tested with Python 2.6, 2.7, 3.3 and 3.4.... 3.9 It should
work with Python greater than 3.4, too.



For Raspberry Pi 4B
----------------------
- if when installing using pip

edit /usr/local/lib/python3.7/dist-packages/Adafruit_DHT/platform_detect.py

add "BCM2711" like below

![image](https://github.com/everylumi/Adafruit_Python_DHT/blob/master/add_code_platform_detect.py.PNG)

    elif match.group(1) == 'BCM2711':
        # Pi 4b
        return 3

- Recommend to Compile and install from this repository 

```sh
git clone https://github.com/everylumi/Adafruit_Python_DHT.git
```

Python 2:

```sh
cd Adafruit_Python_DHT
sudo python setup.py install
```

Python 3:

```sh
cd Adafruit_Python_DHT
sudo python3 setup.py install
```



Installing
----------

### Dependencies

For all platforms (Raspberry Pi and Beaglebone Black) make sure your system is
able to compile and download Python extensions with **pip**:

On Raspbian or Beaglebone Black's Debian/Ubuntu image you can ensure your
system is ready by running one or two of the following sets of commands:

Python 2:

````sh
sudo apt-get update
sudo apt-get install python-pip
sudo python -m pip install --upgrade pip setuptools wheel
````

Python 3:

````sh
sudo apt-get update
sudo apt-get install python3-pip
sudo python3 -m pip install --upgrade pip setuptools wheel
````

### Install with pip

Use `pip` to install from PyPI.

Python 2:

```sh
sudo pip install Adafruit_DHT
```

Python 3:

```sh
sudo pip3 install Adafruit_DHT
```



Usage
-----

See example of usage in the examples folder.



Author
------

Adafruit invests time and resources providing this open source code, please
support Adafruit and open-source hardware by purchasing products from Adafruit!

Written by Tony DiCola for Adafruit Industries.

Modified by LUMI to work at Raspberry Pi 4

MIT license, all text above must be included in any redistribution
