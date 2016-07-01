# FrequencyAnalyzerPhidget
###Description
In order to find the limits of this Phidget 1104_0 Vibration Sensor, a python script was composed to help capture readings from the vibration sensor and analyze them. The script will allow a user to specify a filename to save the data into, as well as the sampling frequency to approximately capture at and the duration of the testing trial. At high sampling frequencies the script becomes a bit troublesome due to small delays in time calculating and data collecting. Using the time.time() function from the time library, we can at least give the user a close approximation on what time the value from the sensor was captured at. The registered values are the timestamp of when a value was captured as well as that value. These two columns saved in the text file can used to graph the sinusoidal graph and calculate the vibration frequency. 

###Hardware
- LabJack U3
- Phidget 1104_0 Vibration Sensor

###Installation
1. Install Git
  1. Windows [Git](https://git-scm.com/)
  2. Linux Users run the command: `sudo apt-get install -y git` or using yum `sudo yum install -y git`
  3. Unix User can use `sudo brew install -y git`
2. Install Libusb-1.0
  1. Windows [Libusb](http://www.libusb.org/wiki/windows_backend) installation steps found there.
  2. Linux: `sudo apt-get install -y libusb-1.0` or `sudo yum install -y libusb-1.0`
  3. Unix users: using Brew `sudo brew install libusb`
3. Install Labjack Driver
  1. Windows [Driver](https://labjack.com/sites/default/files/software/LabJack-2016-05-18.exe)
  2. Linux and Unix users must use the ExoDriver by LabJack:
    1. Clone the respository `git clone https://github.com/LabJack/exodriver.git`
    2. Change directory to the new folder and run the bash file `./install.sh`
4. LabJack Python Library
  1. Clone the repo `git clone https://github.com/LabJack/LabJackPython.git`
  2. Change directory to the new folder and run the setup python file (fun sudo if needed on unix/linux systems): `python setup.py install`
5. Reconnect your LabJack U3 to the computer
6. Clone this repo `git clone https://github.com/xavidram/FrequencyAnalyzerPhidget.git`
  1. Change into the new folder and start analyzing. 
  2. All you have to do is run the python file `python analysis.py`

###License
MIT License

Copyright (c) 2016 Xavid Ramirez

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

###Special Credit
To Luz Sotelo for the huge help learning about how these sensors work and doing all the stress testing on these sensors
