# Climot
> **Technologies:** NodeRed, mqtt, mySQL, XAMPP, Arduino.

Climot is an IoT proyect for a Air conditioner enterprice. The goal is to recieve and display data of the temperature and humidity of the room where the device is located.

**How does it work?**
 First of all, the DHT11 sensor generates temperature and humidity data of the room and sends it to the NodeMCU. Afterwards, the NodeMCU converts the received data to a json format so that it can be sent to to a MQTT broker.
Then, the node.red file recieves the information posted on the MQTT protocol ald displays it to a dashboard so it can plot the data in real time.
Also, NodeRed creates virtual devices and stores the data in a mySQL database created with XAMPP.


**About the files in this repository:**
- *mqtt_esp8266_Base4*:

	This is a folder containing the Arduino file used for the NodeMCU. The program allows the NodeMCU to connect to a WiFi network to send data from the DHT11 sensor to a brokerMQTT in json format.
	
    > **Note:** If the  NodeMCU changes location, you need to modify the internet configuration, shown in lines 24 and 25. In the same way, you must modify the type of sensor and Topic if working with different components.
    

- *iot.sql*:

    Relational database exported from XAMPP in sql format. All the generated data is stored in the "test" table. The "devices" table you will find additional information about the devices that integrate the test table.

- *Node.Red Equipo1 IoT.json*:

    json format document for the Node-red work environment. It is responsible for linking the data received in MQTT with XAMPP and display the dashboard and real time plots. Similarly it allows to simulate 3 types of sensors: 2 autonomous and 1 manual


	
> This proyect was made for my Internet of Things class. 
