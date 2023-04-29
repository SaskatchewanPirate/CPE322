# Lab 5: Paho-MQTT
## From Prof. Lu's GitHub Repo:
### Instructions
1. Study the GitHub [repository](https://github.com/kevinwlu/iot) Lesson 5 labs
2. Install Paho-MQTT
   - On Windows, install [Mosquitto]()
   - Go to System Properties > Environment Variables > Path > New, and enter C:\Program Files\mosquitto
   - Open a terminal
   ```sh
   $ mosquitto_sub -h localhost -v -t test/topic &
   ```
3. Change directory to the iot repository
4. Update the repository with git pull
5. Change directory to Lesson 5
6. Run python3 subcpu.py on one Terminal
7. Run python3 pubcpu.py on another
### [Lesson 5: Paho and Crossbar.io](lesson5/README.md)
