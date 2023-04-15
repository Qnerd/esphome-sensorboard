Installation
============

1. Change Wifi settings in secrets.yaml

2. firmware flashing with docker image over USB. (Change ttyUSB0 to your devicename. for example ttyACM0):
	docker run --rm -v "${PWD}":/config --device=/dev/ttyUSB0 -it esphome/esphome run sensor.yaml


Additional (useful) commands:
=============================

logging:
	docker run --rm --net=host -v "${PWD}":/config -it esphome/esphome

OTA Update:
#  qnerd-sensor.local must be resolvable via DNS. try to add it to your /etc/hosts with the correct IP
	docker run --rm --net=host -v "${PWD}":/config -it esphome/esphome run sensor.yaml

