* Install BCM2835 libraries

wget http://www.airspayce.com/mikem/bcm2835/bcm2835-1.60.tar.gz
tar zxvf bcm2835-1.60.tar.gz 
cd bcm2835-1.60/
sudo ./configure
sudo make
sudo make check
sudo make install
#For more details, please refer to http://www.airspayce.com/mikem/bcm2835/

* Install Wiring PI

sudo apt-get install wiringpi

#For Pi 4, you need to update it：
cd /tmp
wget https://project-downloads.drogon.net/wiringpi-latest.deb
sudo dpkg -i wiringpi-latest.deb
gpio -v
#You will get 2.52 information if you install it correctly

* Intall Python libraries

#python2
sudo apt-get update
sudo apt-get -y install python-pip
sudo apt-get -y install python-pil
sudo apt-get -y install python-numpy
sudo pip install RPi.GPIO
sudo pip install spidev
#python3
sudo apt-get update
sudo apt-get -y install python3-pip
sudo apt-get -y install python3-pil
sudo apt-get -y install python3-numpy
sudo pip3 install RPi.GPIO
sudo pip3 install spidev

#Examples
sudo git clone https://github.com/waveshare/e-Paper
cd e-Paper/RaspberryPi\&JetsonNano/