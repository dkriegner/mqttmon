# mqttmon - MQTT text based user interface monitor

A primitive TUI tool to show the messages received from a MQTT broker. The main difference to mosquitto_sub or other CLI tools which are able to connect to a MQTT broker is that it allows different view/update modes and scrolling in the message list.

Supported view modes are:

* continuous: lists messages as received
* inplace: lists only the last message per topic
* topics: lists topics and messages per topic upon selection
* details: by selecting one message details about this message are shown (retain, QOS-flag, receiving time)

A screenshot of the default view is shown below:

![mqttmonitor screenshot](https://raw.githubusercontent.com/dkriegner/mqttmon/master/screenshot.png?raw=true "screenshot")

Currently not support for sending messages is included nor planned!

## Installation

download script and put it in any folder of your convenience.

## Usage

Starting the TUI is done by:

	mqttmon test.mosquitto.org
    
Command line options are:

    usage: mqttmon [-h] [-c conffile] [-p port] [-u username] [-P passwd]
                   [-t topic]
                   [brokeraddress]
    
    curses TUI for MQTT message monitoring
    
    positional arguments:
      brokeraddress         Address of the MQTT broker
    
    optional arguments:
      -h, --help            show this help message and exit
      -c conffile, --config conffile
                            specify config file
      -p port, --port port  TCP port for the MQTT broker
      -u username, --user username
                            user name for the broker connection (empty if not
                            needed)
      -P passwd, --pass passwd
                            password for the broker connection (empty if not
                            needed)
      -t topic, --topic topic
                            topics to subscribe


The programm needs at least the server address of the Broker. Settings can also be made in a ini-style config file.

An example config file for [test.mosquitto.org](http://test.mosquitto.org/) could look like

    [Defaults]
    port = 1883
    #username = user
    #passwd = password
    topic = #
    brokeraddr = test.mosquitto.org


## Status

The project is in beta-phase. Might need improvements but is basically usable! A list of things which need fixing can be found in a TODO file.

### Dependencies

This script is written in Python and therefore needs

* [Python 3.X](https://www.python.org/downloads) and 
* the [paho-mqtt](https://pypi.python.org/pypi/paho-mqtt) package (>v2.0)
