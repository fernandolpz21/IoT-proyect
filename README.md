# IoT-proyect
This is the proyect that i made for my Internet of Things Class
The goal of the proyect is to recive the values of the temperature and humidity via the DHT11 sensor so the NodeMCU could recieve them. Then it converts the data to a json format so it can send it to the MQTT broker.
The node.red file then recieves the information in the MQTT, displays it to a dashboard and stores the data in a database created in XAMPP

-> mqtt_esp8266_Base4:
    Folder containing the Arduino file used for the NodeMCU.
    You need to upload to the NodeMCU via a USB/microUSB cable. If the NodeMCU changes location, you need
    modify the internet configuration, shown in lines 24 and 25. In the same way, you must modify
    the type of sensor and Topic if working with different components
    The program allows the NodeMCU to connect to a WiFi network to send data from the DHT11 sensor to a brokerMQTT
    in json format

-> iot.txt:
    Database exported from XAMPP in sql format. In the test table all the
    data stored in the database and in the devices table you will find additional information about the
    devices that integrate the test table

-> Node.Red Equipo1 IoT.json:
    json format that allows the Node-red work environment to be able to read information about a structure of nodes to
    can be used and modified later.
    It is responsible for linking the data received in MQTT with XAMPP and with the dashboard in real time. Similarly
    allows to simulate 3 types of sensors: 2 autonomous and 1 manual
