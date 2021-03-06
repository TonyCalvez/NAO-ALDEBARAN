# NAO-ALDEBARAN

Video to install :  https://youtu.be/yOC8jpNYSzQ </br>
Video to compile : https://youtu.be/-7ceG7AA1Do

## To Install C++ SDK - ALDEBARAN


### 0) Install: Choregraphe
```
-> Online : https://developer.softbankrobotics.com/us-en/downloads/pepper 
```


### 1) The pre-requisites </br>
```
-> sudo apt-get install build-essential checkinstall 
-> sudo apt-get install gcc-multilib libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libc6-i386 libbz2-dev 
```


### 2) Install: Python 2.7 (only) + CMake + QTCreator </br>
```
-> sudo apt-get install gcc cmake qtcreator 
-> cd /usr/src 
-> wget https://www.python.org/ftp/python/2.7.13/Python-2.7.13.tgz 
-> tar xzf Python-2.7.13.tgz 
-> cd Python-2.7.13 
-> sudo ./configure 
-> sudo make altinstall 
```


### 3) Install: SDK Naoqi </br>
```
-> Online : https://developer.softbankrobotics.com/us-en/downloads/pepper
```

### 4) Install: qiBuild </br>
```
-> sudo apt install python-pip
-> pip install qibuild
```
```
  If qiBuild doesn't launch: 
	-> gedit ~/.bashrc and in the end of the file add: export PATH=${PATH}:${HOME}/.local/bin
```

## To Config C++ SDK - ALDEBARAN
### 5) Configuration: qiBuild Toolchains </br>
```
-> qibuild init --interactive 
-> qitoolchain create linux <path/to/cpp/sdk>/toolchain.xml
-> qitoolchain create mytoolchain <path/to/cpp/sdk>/toolchain.xml
-> qibuild add-config mytoolchain -t mytoolchain
-> qitoolchain info
```

## To Compile the Program C++ with the SDK - ALDEBARAN
### 6) Workspace : Helloworld </br>
```
-> cd /usr/src/workspace
-> qibuild config --wizard
-> qibuild configure -c mytoolchain
-> qibuild make -c mytoolchain
```

## To Launch the Program with the C++ - ALDEBARAN
### 7) Start the Project </br>
```
-> cd /usr/src/areacompilation
-> ./helloworld --pip <robot_ip> --pport <robot_port>
```

Link: https://www.uv.mx/anmarin/papers/NAO_Tutorial.pdf
Link: http://dhrc.snu.ac.kr/nao-1-14-installation-guide-on-ubuntu-12-04/
