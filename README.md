MyCeli is a mesh network based on Nebula currently.
This is intended to grow to act as a communication tool
and a community supported cloud space.

Installation:

RasperryPi
Download and install latest light PiOS image
https://www.raspberrypi.org/software/operating-systems/

Enable SSH by creating a "ssh" empty file in the root of the "boot" partition

SSH to pi@raspberrypi with default password "raspberry"

run raspi-config and change pi password and host name

after autoreboot run 
sudo apt update
sudo apt upgrade
sudo apt install git
sudo apt install vim
sudo apt install openvpn

git clone https://github.com/groundfoundation/myceli.git ~
mkdir /opt/myceli
Copy ~/myceli/nebula_build/linux_amd64/nebula /opt/myceli 
Copy ca.crt /opt/myceli
copy myceli.* /opt/myceli
copy config.yaml /opt/myceli
cd /opt/myceli
sudo ./nebula -config ./config.yaml


Needed for Lighthouse:
ufw allow from any proto udp to any port 4242

Needed for Tethered Pi

