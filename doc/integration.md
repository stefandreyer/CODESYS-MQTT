
# How To and Dokumentation

## __Gerneral__

- after creating a new project you need to add the library

<img src="../_img/ADD_Lib.png" width="350">

- then you have to activate dynamic memmory allocation

- right click on Application, then Option Application 

<img src="../_img/DynMemmory.png" width="350">

## __BASIC Handler__

- you need a struct of __SD_MQTT.MQTT_IN_OUT__ and a instance of __SD_MQTT.HANDLE_MQTT__ for communication to the broker
- this setup will comunicate to teh broker but does not send or receive publish packets

<img src="../_img/HandleMQTT.png" width="350">

## __DEBUGGING__

- in case of trobble, there is in the __SD_MQTT.HANDLE_MQTT__ instance a __ErrorHistory__ , there you will finds hints

<img src="../_img/ErrorHistory.png" width="350">

## __first publish__

- FirstPublish FB, need to check publish....
- make a instance of __SD_MQTT.MQTTPublish__
- you have to call __SET_MQTT_IN_OUT__ once, there your __SD_MQTT.MQTT_IN_OUT__ struct is the parameter
- call the instance, there you can define the topic, payload, QoS, retain
-- payload can be a string or a byte array, for the array you must provide the length
-- selection of string or array is done by the input __PublishAsString__ (True --> String, False --> Array)
- by setting the input __send__ to True, the packet is published
- use __done__ for checking if the transmit is done
- you can instance as much instances of __SD_MQTT.MQTTPublish__ as you like, the Library is coordinading the rest
- the __SD_MQTT.HANDLE_MQTT__ FB atually is set up to handle 50 incomming and outgoing packets per second
 
<img src="../_img/FirstPublish.png" width="350">