
Python library to read the DHT series of humidity and temperature sensors on a
Raspberry Pi or Beaglebone Black.

Designed specifically to work with the Adafruit DHT series sensors ---->
https://www.adafruit.com/products/385

Currently the library is tested with Python 2.6, 2.7, 3.3 and 3.4.... 3.9 It should
work with Python greater than 3.4, too.

## For Raspberry Pi 4B
----------------------
- edit /usr/local/lib/python3.7/dist-packages/Adafruit_DHT/platform_detect.py
add "BCM2711" like below

![image](https://user-images.githubusercontent.com/75207648/136056520-a0487fe2-1ceb-410b-96b3-eb1e9260c228.png)

    elif match.group(1) == 'BCM2711':
        # Pi 4b
        return 3

- or Compile and install from this repository 
  git clone https://github.com/everylumi/Adafruit_Python_DHT.git


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

### Compile and install from the repository

First download the library source code from the [GitHub releases
page](https://github.com/adafruit/Adafruit_Python_DHT/releases), unzipping the
archive, and execute:

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

## Recommand git clone the repository
You may also git clone the repository if you want to test an unreleased
version: 

```sh
git clone https://github.com/everylumi/Adafruit_Python_DHT.git
```

Usage
-----

See example of usage in the examples folder.

Author
------

Adafruit invests time and resources providing this open source code, please
support Adafruit and open-source hardware by purchasing products from Adafruit!

Written by Tony DiCola for Adafruit Industries.

Modified by LUMI to work for Raspberry Pi 4

MIT license, all text above must be included in any redistribution
