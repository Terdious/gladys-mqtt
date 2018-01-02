Gladys MQTT# gladys-mqtt This module connect 
Gladys to a MQTT broker, in order to support 
Owntrack, an open-source (and awesome) location 
tracker. Need Gladys version >= 3.0.0. 
Documentation To make this module work in Gladys, 
you need to : First, install the module Without 
rebooting, just set three global parameters in 
"Param" view in the dashboard : MQTT_URL => The 
URL of the MQTT broker, for example : 
"mqtt://xxxx.cloudmqtt.com:19692" MQTT_USERNAME 
=> The username to connect to the MQTT broker 
MQTT_PASSWORD => The password of the MQTT user 
Reboot Gladys. In the logs you should see 
"Successfully connected to MQTT : 
YOUR_SERVER_URL" This should looks like this : 
Gladys parameters Set up a MQTT broker
To set up your MQTT broker, you have two options 
:
Install your own MQTT on your server or your 
Raspberry Pi Use a third-party MQTT Cloud To test 
this module in Gladys, I used CloudMQTT, the 
service is free up to 10 connections, so that's 
fine to test. CloudMQTT If you want to use 
CloudMQTT, just create an account, confirm your 
email, then create an instance. This should looks 
like this : Cloud MQTT You could now fill this 
infos in Gladys. MQTT_URL = 
mqtt://xxxx.cloudmqtt.com:PORT MQTT_USERNAME = 
User in info panel MQTT_USERNAME = Password in 
info panel Owntrack To play with owntrack to save 
your location in Gladys, you need to install the 
iOS or Android app. In Preferences, go to 
Connection: Mode => "Private MQTT", Host => Host 
= xxxx.cloudmqtt.com Port = SSL PORT (be careful, 
that's not the same port as before) 
Identification => Username => MQTTT username 
Password => MQTT Password Device ID => "whatever 
you want, name of your phone for example" Tracker 
ID => Your UserID in Gladys (very important !), 
or the UserID you want to track
Then save, and you should see the message 
"Connected".
