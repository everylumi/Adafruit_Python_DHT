
# Adafruit_Python_DHT
Python library to read the DHT series of humidity and temperature sensors on a
Raspberry Pi or Beaglebone Black.

Designed specifically to work with the Adafruit DHT series sensors ---->
https://www.adafruit.com/products/385

Currently the library is tested with Python 2.6, 2.7, 3.3 and 3.4.... 3.9 It should
work with Python greater than 3.4, too.


## Installation
```sh
cd Downloads/  
git clone https://github.com/everylumi/Adafruit_Python_DHT.git
cd Adafruit_Python_DHT/
sudo python3 setup.py install #Python3  
sudo python setup.py install #Python2
```


## what if install using pip at Raspberry Pi 4B
- edit "platform_detect.py" for using  
```
/usr/local/lib/python3.7/dist-packages/Adafruit_DHT/platform_detect.py
```
- add "BCM2711" like below

```python
    if not match:
        # Couldn't find the hardware, assume it isn't a pi.
        return None
    if match.group(1) == 'BCM2708':
        # Pi 1
        return 1
    elif match.group(1) == 'BCM2709':
        # Pi 2
        return 2
    elif match.group(1) == 'BCM2835':
        # Pi 3
        return 3
    elif match.group(1) == 'BCM2837':
        # Pi 3b+
        return 3
    #add 'BCM2711'
    elif match.group(1) == 'BCM2711':
        # Pi 4b
        return 3
    else:
        # Something else, not a pi.
        return None

    elif match.group(1) == 'BCM2711':
        # Pi 4b
        return 3
```


## Installing using pip
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


## Usage
See example of usage in the examples folder.



## Author
Adafruit invests time and resources providing this open source code, please
support Adafruit and open-source hardware by purchasing products from Adafruit!

Written by Tony DiCola for Adafruit Industries.

Modified by LUMI to work at Raspberry Pi 4

MIT license, all text above must be included in any redistribution
