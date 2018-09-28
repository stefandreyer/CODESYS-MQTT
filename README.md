# CODESYS-MQTT
MQTT client for CODESYS

# Dependencies

all needed Libraries can be found at
  
  https://github.com/stefandreyer

# Features
- all QoS Levels for publish and subscribe
- will topic
- retain option for publish and will topic
- unlimited publish FBs(by library)
- unlimited subscribe FBs(by library)
- TLS support(without certificates)
- FBs for easy transmit of values and states

# New value FB

created an new FB for easy publishing Values to broker

# New Stats FB

created new FB for easy publishing stats(on/off, true/false) to broker

# Will topic

will topic is now build with client id

# Examples

nice example projets for Windows and RaspberryPi with and without TLS using test.mosquitto.org, so no own broker needed
