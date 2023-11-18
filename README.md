# The IoT Sensor Data Collection and Visualization project 
## Introduction
Several days ago, I decided to challenge myself by creating an IoT project and learning more about integrating end devices into a cloud environment. Given budget constraints, I could not spend resources on this project. To achieve my goal, I used some electronic components that I already had and free cloud services.
## Description: 
In this project the main objective is to  collect environmental data from sensors, process the information, and provide interactive data visualizations.
It uses an ESP32 microcontroller with temperature, pressure, humidity, and sunlight sensors to gather real-time data. The collected data is then sent to an MQTT broker, which triggers an AWS Lambda function to extract and process the sensor measurements using Python. The processed data is then stored in an Atlas MongoDB database, and Tableau is used to create data representations.
![](/Images/Diagram.png)

## Components of the Project

#### ESP32 Microcontroller

The ESP32 microcontroller, the core hardware component of the project, connects to four sensors: temperature, pressure, humidity, and sunlight sensors. The ESP32 acts as the data collection node, continuously capturing sensor measurements and packaging them for transmission with an RTC (Real Time Clock) coupled to provide the basis of time for timestamping.
![](/Images/MeterStation.JPG)

#### MQTT Broker
The ESP32 sends the collected data to an MQTT broker. MQTT (Message Queuing Telemetry Transport) is a lightweight messaging protocol designed for efficient communication between IoT devices and servers. It ensures that data is transmitted efficiently from the ESP32 to the cloud.

#### AWS Lambda Function
Upon receiving data from the MQTT broker, an AWS Lambda function is invoked. This serverless computing service uses Python code to process the sensor data, extract relevant measurements, and prepare the data for storage in a database in Json format.


#### Atlas MongoDB Database
The processed sensor data is written to an Atlas MongoDB database and provides a structured repository for the collected measurements.


#### Tableau Data Visualization
he final step in the project involves using Tableau to create interactive and insightful data visualizations based on the data collected from the sensors. 



#### Prelimirary Results
---------------------

![](/Results/dataset.png)

------------------------

![](/Results/equation.png)

------------------------
![](/Results/parameters.png)

------------------------

![](/Results/Esp01.png)

------------------------

![](/Results/confint.png)

------------------------

![](/Results/Humid.png)

-----------------------

![](/Results/Temp.png)

----------------------

![](/Results/grafico3D.png)

----------------------

![](/Results/Correlation.png)

----------------------

![](/Results/scatter_fitted.png)

-----------------------













