# Lab 5: Paho-MQTT
### [Results](Results.md)
## From Prof. Lu's GitHub Repo:
### Instructions
1. Study the GitHub [repository](https://github.com/kevinwlu/iot) Lesson 5 labs
2. Install Paho-MQTT
   - On Windows, download and install [Mosquitto](mosquitto-2.0.15-install-windows-x64.exe)
   - Go to System Properties > Environment Variables > Path > New, and enter C:\Program Files\mosquitto
   - Open a terminal
   ```sh
   $ cd 'C:\Program Files\mosquitto'
   $ net start mosquitto
   $ .\mosquitto_sub -h localhost -v -t 'test/topic'
   ```
   - Open a second terminal
   ```sh
   $ cd 'C:\Program Files\mosquitto'
   $ .\mosquitto_pub -h localhost -t 'test/topic' -m "Hello"
   ```
   - Return to the first terminal and CTRL-C
   ```sh
   $ python -m pip install paho-mqtt
   $ git clone https://github.com/eclipse/paho.mqtt.python.git
   ```
3. Change directory to the iot repository
4. Update the repository with git pull
5. Change directory to Lesson 5
   ```sh
   $ cd ~\iot\lesson5
   ```
6. Run python3 subcpu.py on one Terminal
   ```sh
   $ py -3.9 subcpu.py
   ```
7. Run python3 pubcpu.py on another
   ```sh
   $ cd ~\iot\lesson5
   $ py -3.9 pubcpu.py
   ```
### [Lesson 5: Paho and Crossbar.io](lesson5/README.md)
