# GROW BOX  

<p float="left">
<img src="https://github.com/emb-growbox/.github/blob/main/profile/groboximage.jpeg" alt="drawing" width="300" height="300"/>
<img src="https://github.com/emb-growbox/.github/blob/main/profile/groboxside.jpeg" alt="drawing" width="300" height="300"/>
</p>



GROW BOX was made to control and monitor a home plant.
Our project uses several sensors to monitor the plant and shows this data on a well-designed web site.

In addition, you can control the light and the irrigation from the website. 

<img src="https://github.com/emb-growbox/.github/blob/main/profile/UI1.JPG" alt="drawing"/>

Moreover, you can also check our cool graphs that show you the data from the past week.

<img src="https://github.com/emb-growbox/.github/blob/main/profile/UI2.JPG" alt="drawing"/>


## Requirements

### Hardware Requirements

- MSP432 
- Node MCU
- Soil Moisture Sensor
- DHT Sensor
- Ultrasonic Sensor
- Power Supply
- LED Strip
- Stepper motor
- Wires
- 3d printer


### Software Requirements

- Energie IDE
- Arduino IDE
- Node js installed


## Project Layout
```
├── emb-grow-box
    ├── emb-growbox-msp 
            ├── Timer.cpp   #Timer interrupt helper
            ├── Timer.h  
            ├── tuttoetutto.ino # source code
    ├── emb-grow-box-arduino 
            ├── new_arduino_wifi.ino # source code 
    ├── emb-growbox-client 
            ├── build   
            ├── public   
            ├── src   #source code
                ├── .... all client code 
            ├── stuff 
            ├── .gitignore
            ├── package.json
            ├── tailwind.config.js
```

## How to Build,Burn and Run

### MSP:
#### Build:
Libraries:
- Adafruit_Sensor.h
- DHT.h
- DHT_U.h
- Stepper.h
- Timer.h (Included with the code)

Comunication connections:
- Connect pin #3 (rx) of MSP to pin D8 (tx) of NodeMCU 
- Connect pin #4 (tx) of MSP to pin RX of NodeMCU
Sensors connections on the MSP432:
- Soil humidity analog connector -> pin #6
- Temperature and air humidity digital -> pin #5
- Ultrasonic sensor pins: TRIG -> #9 ECHO -> #10
- Light controller: WHITE -> #18 BLUE/RED -> #19
- Stepper motor: IN1 -> #24 IN2 -> 25 IN3 -> 29 IN4 -> 30

#### Burn:
-
    Burn using Energie IDE  


### NodeMCU:
#### Build:
-
    Install ESP8266WiFi, Firebase_ESP_Client, NTPClient & SoftwareSerial libraries.

-  Change the Wifi credentials.
    

#### Burn:

- Burn using Arduino IDE  
 

### Client:
    Run: 
    npm install
    npm start


