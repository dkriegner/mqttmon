# mqttmon - MQTT text based user interface monitor

A primitive TUI tool to show the messages received from a MQTT broker. The main difference to mosquitto_sub or other CLI tools which are able to connect to a MQTT broker is that it allows different view/update modes and scrolling in the message list.

A screenshot of the default view is shown below:

![mqttmonitor screenshot](https://raw.githubusercontent.com/dkriegner/mqttmon/master/screenshot.png?raw=true "screenshot")

Currently not support for sending messages is included!

## Installation

download script and put it in any folder of your convenience.

## Usage

Starting the TUI is done by:

	mqttmonitor

Currently the programm does not accept any arguments. The server settings need to be made in the top of the script by changing some global variables.

## Status

The project is pre-alpha. Not yet user friendly and likely to contain serious
bugs! A list of important things to be fixed can be found in a TODO file.

### Dependencies

This script is written in Python and therefore needs

* [Python 3.X](https://www.python.org/downloads) and 
* the [paho-mqtt](https://pypi.python.org/pypi/paho-mqtt) package
