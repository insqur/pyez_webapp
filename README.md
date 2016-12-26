## Web application used PyEZ + Flask
====


## Overview


This application can search Junos Devices , change configuretions and show device informations about multi devices.


Juniper PyEZを用いたWebアプリケーションを実装しています。


指定したアドレス範囲内でJunosデバイスを探索し、複数台のデバイスに対する設定の変更や情報の取得を行います。


## Features
* デバイスとの接続と情報の取得
* 任意のデバイスの情報の表示
* 設定情報の一括変更
* 取得情報を基にしたトポロジの可視化


* Connect to Junos devices and collect device informations 
  
  ![connect](https://github.com/thanzawa/figures/blob/master/pyez_webapp/connect.PNG "connect_device")

* Show device informations at selected devices

  ![show devices](https://github.com/thanzawa/figures/blob/master/pyez_webapp/show_devices.PNG "show_device")

* Change configurations at selected devices
  
  ![send command](https://github.com/thanzawa/figures/blob/master/pyez_webapp/set_commands.PNG "send_commands")

* Visualization of network topology using PyEZ, NetworkX, Matplotlib, mpld3

  ![topology](https://github.com/thanzawa/figures/blob/master/pyez_webapp/topology2.png "topology")
  
  ![info](https://github.com/thanzawa/figures/blob/master/pyez_webapp/detailed_info.PNG "detailed_info")



## Requirements

* Server

  Installing Python 2.6 or 2.7, and Junos PyEZ.

  For more information, please refer to URL below.

  <http://www.juniper.net/techpubs/en_US/junos-pyez1.0/topics/task/installation/junos-pyez-server-installing.html>

  I developed and tested this application at Ubuntu 14.04 LTS 32bit. 

  So, I reccomend the use of Ubuntu

* Junos Devices

  Enable NETCONF and lldp

  `set system services netconf ssh`

  `set protocols lldp interface all`

## Install

* Install libraries

  `sudo pip install -r requirements.txt`
  
  (If you get the error at matplotlib, please run the following command)
  
  `sudo apt-get install python-numpy python-scipy python-matplotlib`


* Run

  `python app.py`
  
  You can access to "http://127.0.0.1:5000"



