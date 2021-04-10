# esp32_timer_group_example
Ported from github "CalinRadoni/ESP32Timers" and "CalinRadoni/ESP32HAL" example

Original source:
https://github.com/CalinRadoni/ESP32Timers
https://github.com/CalinRadoni/ESP32HAL

But build failed at my ESP-IDF setup. So copy .cpp/.h files to ESP-IDF project template and works well.

-------------
# How To build:
* Setup ESP-IDF - following tutorial:
* Install Prerequisites: https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/linux-setup.html
* sudo apt-get install git wget flex bison gperf python python-pip python-setuptools cmake ninja-build ccache libffi-dev libssl-dev dfu-util

* Get ESP-IDF https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/index.html#get-started-get-esp-idf
* cd ~/esp
*git clone -b v4.2 --recursive https://github.com/espressif/esp-idf.git
* cd ~/esp/esp-idf
* ./install.sh

## setup environment
* . $HOME/esp/esp-idf/export.sh
* alias get_idf='. $HOME/esp/esp-idf/export.sh'
(add to .bashrc)

## Project creation:
* get_idf
* idf.py create-project --path my_projects my_new_project

## Project setup:
* idf.py set-target esp32
* idf.py menuconfig
* idf.py -p /dev/ttyUSB0 flash monitor 2>&1 | tee log1.txt




