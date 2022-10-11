# ESE519lab-guide


## 
platform:
OS: macOS  Version 11.6
Processor: Apple M1 
 MacBook Air (M1, 2020)
 
##
1install homebrew

$ /bin/bash -c "$(curl -fsSL
https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"



2install arm-none-eabi-gcc

![image](https://user-images.githubusercontent.com/114256663/194977725-95747296-00ea-4787-89a5-b4c4c501fd9d.png)


3install Terminal_Rosetta2
$ /usr/sbin/softwareupdate --install-rosetta --agree-to-license

![image](https://user-images.githubusercontent.com/114256663/194977768-24ef5a57-0c18-4d02-9309-c9a582534c65.png)


4install VScode (google)

5install the CMake Tools
![image](https://user-images.githubusercontent.com/114256663/194978120-9183bff8-120c-446c-ab85-e73c07dc6cf8.png)

6create .vscode file

{
  "cmake.environment": {
  "PICO_SDK_PATH": "../../pico-sdk"
  },
  "C_Cpp.default.configurationProvider": "ms-vscode.cmake-tools"
}
![image](https://user-images.githubusercontent.com/114256663/194979294-78a60a4a-8050-482b-997a-71ad418c1e7b.png)

7  configure as follows:

![image](https://user-images.githubusercontent.com/114256663/194979757-59441ff9-97ac-40db-ae3f-8526d975edd8.png)

![image](https://user-images.githubusercontent.com/114256663/194980059-582af3f4-e39b-47a0-8b97-b96a53db8625.png)


8called pico

![image](https://user-images.githubusercontent.com/114256663/194980578-27024a66-67be-4c89-bf25-dbb0631e1367.png)
$ cd ~/
$ mkdir pico
$ cd pico
![image](https://user-images.githubusercontent.com/114256663/194980860-f6b48d56-41a6-448d-8109-50dfef2a74fc.png)$ git clone -b master 

$ cd pico-sdk
$ git submodule update --init
$ cd ..
$ git clone -b master 

![image](https://user-images.githubusercontent.com/114256663/194981156-73636b56-0c0a-48d3-9575-bf3f2d8af62d.png)
$ cd pico-examples
$ mkdir build
$ cd build

9input code as follows in the file "hello_usb.uf2"

$ cd build
$ cd hello_word
$ make -j8

![image](https://user-images.githubusercontent.com/114256663/194981482-78723bc5-ed78-46ca-8cb5-3bfde93c6bb0.png)

10 insert the chip 
press and hold the reset ,press the reboot 
![image](https://user-images.githubusercontent.com/114256663/194982734-ed6c9395-cc92-4dfc-8fc6-696174ca2377.png)



11 input
$ ls dev/tty.*
then unplug the chip 
you can see which file you lose
then insert the chip again
input 
$ screen /dev/tty.usbmodem1101 115200
![image](https://user-images.githubusercontent.com/114256663/194982466-a3007b03-11e8-468d-892e-3099be603142.png)


12 input 
$ hello world  
in the VScode
![image](https://user-images.githubusercontent.com/114256663/194983667-84f98f4b-dfb3-42a0-b625-b2e0363da1e5.png)

13 the screen will show as follows:
![image](https://user-images.githubusercontent.com/114256663/194983775-47cd5e7c-ea52-45e5-bb04-70060de816ac.png)






































