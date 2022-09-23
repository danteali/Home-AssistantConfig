# Home Assistant Configuration

This repo 'should' contain an always up to date record of my Home Assistant configuration. 

It is automatically updated as part of my config deployment process after I make any changes and verify that the configuration is valid.

Note that all my services run in Docker and my 'home automation stack' is comprised of:
* Home Assistant
* Node Red
* Eclipse Mosquitto MQTT Broker
* Zigbee2MQTT
* TasmoAdmin

Old docker service scripts can be found [in this repo](https://github.com/danteali/DockerRunFiles) with the services running the 'home automation stack' in the [/monitoring/homeassistant](https://github.com/danteali/DockerRunFiles/tree/master/monitoring/homeassistant) folder. 

Have since moved to a docker-compose based configuration which will be updated in a repo in due course. 

I used to script all my home automations using the Home Assistant 'automations' functionality but have migrated onto using Node Red to set up and manage all my automations. It is much more intuitive to use and has loads of 'palettes' which can add additional functionality e.g. Slack notifications, Alexa integration, ...

I have various components configured in Home Assistant and mainly use the 'packages' functionality to keep the configuration for each set of components together (e.g. all IKEA Tradfri entities set up in one place) as it helps me logically separate and track the configuration more easily instead of spreading them and having them defined across multiple yaml files (e.g. Ikea switches and Nest switches mixed together in the switches.yaml file).

I have also used a number of 'Custom Components' which are effectively unofficial Home Assistant components. Some of which will probably end up integrated in the main Home Assistant service. The custom component files have not been included in this repo since they change often and are easily obtained from the developer's github pages. The custom components themselves are configured in the configuration.yaml file or in the 'packages' folder. The configuration will provide the necessary info on where to go to find the custom component.

Below is a [quick and dirty diagram](https://app.creately.com/diagram/PrbMeype7UP/view) of how the Docker services and automation components fit together...

![HomeAutomation](https://raw.githubusercontent.com/danteali/Home-AssistantConfig/master/HomeAutomation.png)