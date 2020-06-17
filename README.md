#Mqtt Monitoring With Zabbix

This template created for monitoring Mqtt message broker v2.3 (any version that uses management api v2) and tested on zabbix server v4.2 but it probably works on other versions.

Installation

1.Upload userparameter file to zabbix agent directory that is included in agent’s config file and restart agent.

2.Upload template file to zabbix server. Add template to host that has mqtt running.

3.Add these macros in host configuration:

{$MQTT_IP} => Mqtt server ip address

{$MQTT_PORT} => Mqtt running port

{$MQTT_USER} => Mqtt username

{$MQTT_PASS} => Mqtt password

After few moments you can see that items are getting values in Last data page.

I’m still wotking to imporve the template and create this template for other Mqtt versions.
