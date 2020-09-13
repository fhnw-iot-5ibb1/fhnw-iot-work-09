# IoT Engineering
## Hands-on of lesson 9
For slides and example code, see [lesson 9](../../../fhnw-iot/blob/master/09/README.md)

> *Note: Do not work on this repository right away.*<br/>
> *[Check existing forks to find the specific repository for your class.](../../network/members)*

### a) Dashboard as a service, 15'
* Choose a dashboard service and a transport protocol, try [ThingSpeak](https://thingspeak.com/), [Cayenne](https://cayenne.mydevices.com/) or [ThingsBoard.io](https://thingsboard.io/).
* Check the API docs to understand the payload format.
* Send data "as a device" with curl or with the mqtt CLI.
* The CLI runs on the Raspberry Pi or on your laptop.

### b) Glue code, 15'
* Configure the [TTN to ThingSpeak adapter](https://github.com/tamberg/fhnw-iot/blob/master/09/Now/TtnToThingSpeakAdapter/index.js) glue code.
* Create a free account and host the code on [Zeit Now](https://zeit.co/).
* Use curl to simulate calls from the TTN backend:<pre>
$ curl -v http://127.0.0.1:8080/ --data '{"app_id":"fhnw-iot","dev_id":"fhnw-iot-arduino-1","payload_raw": "FwAqAA=="}' # Base64</pre>
* Replace 127.0.0.1:8080 with your Zeit Now URL.

### c) Docker hosted dashboard, 15'
* Install Docker on your computer (not Raspberry Pi).
* Run InfluxDB and run/create a Grafana dashboard.
* Run Telegraf to get data from test.mosquitto.org.
* Send data "as a device" with mqtt, to Mosquitto.
