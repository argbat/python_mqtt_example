# Installing an MQTT Broker on Your Machine

In this guide, we will install and set up the Mosquitto MQTT broker, a lightweight broker ideal for targeting Raspberry Pi devices.

## Installation on macOS

To install Mosquitto on macOS, use Homebrew:

```sh
brew install mosquitto
```

## Setting Up a Python Environment

1. **Create a Virtual Environment**

   Navigate to your project directory and create a virtual environment:

   ```sh
   cd <proj_dir>
   python3 -m venv .env
   ```

2. **Activate the Virtual Environment**

   ```sh
   source .env/bin/activate
   ```

3. **Install Python MQTT Client Library**

   Install the Paho MQTT client library using pip:

   ```sh
   pip install paho-mqtt
   ```

## Running the Code

1. **Start the MQTT Broker**

   Open a new terminal and start the Mosquitto broker:

   ```sh
   mosquitto -v
   ```

2. **Run the Subscriber Script**

   In another new terminal, navigate to your project directory and run the subscriber script:

   ```sh
   cd <proj_dir>
   python3 mqtt_sub.py
   ```

3. **Run the Publisher Script**

   In yet another new terminal, navigate to your project directory and run the publisher script:

   ```sh
   cd <proj_dir>
   python3 mqtt_pub.py
   ```

You should now see the messages being published by the `mqtt_sub.py` script and received by the `mqtt_pub.py` script in real-time.
