# raspiledcontrol
# Install raspi OS
sudo apt-get update
sudo apt-get upgrade
# Install adafruit control libraries
sudo pip3 install rpi_ws281x adafruit-circuitpython-neopixel
sudo python3 -m pip install --force-reinstall adafruit-blinka


# clone the animation code
git clone https://github.com/adafruit/Adafruit_CircuitPython_LED_Animation.git


# change code to match setup
find ./ -type f -exec grep -H 'board.' {} \;
find ./ -type f -exec sed -i 's/board.A1/board.D18/gI' {} \;
find ./ -type f -exec sed -i 's/board.A1/board.D18/gI' {} \;
find ./ -type f -exec sed -i 's/board.A3/board.D18/gI' {} \;
find ./ -type f -exec sed -i 's/board.D6/board.D18/gI' {} \;
find ./ -type f -exec sed -i 's/board.D3/board.D18/gI' {} \;
find ./ -type f -exec sed -i 's/board.D5/board.D18/gI' {} \;
find ./ -type f -exec grep -H 'pixel_num =' {} \;
find ./ -type f -exec sed -i 's/pixel_num = 32/pixel_num = 90/gI' {} \;
find ./ -type f -exec sed -i 's/pixel_num = 30/pixel_num = 90/gI' {} \;
find ./ -type f -exec sed -i 's/pixel_num = 64/pixel_num = 90/gI' {} \;