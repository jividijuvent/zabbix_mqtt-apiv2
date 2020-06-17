# Mqtt Monitoring With Zabbix

This template created for monitoring Mqtt message broker v2.3 (any version that uses management api v2) and tested on zabbix server v4.2 but it probably works on other versions.

# Items

List of items that you can monitor:


    packets/publish/received
    packets/pubrel/received
    packets/puback/missed
    packets/disconnect
    packets/pingreq
    packets/pubrec/sent
    messages/qos1/received
    bytes/sent
    packets/unsuback
    packets/pubrec/received
    messages/qos0/received
    messages/qos1/sent
    messages/qos2/dropped
    packets/puback/received
    packets/sent
    packets/publish/sent
    messages/qos0/sent
    packets/connect
    packets/received
    messages/sent
    bytes/received
    messages/qos2/received
    packets/pubrel/sent
    packets/suback
    packets/connack
    messages/dropped
    packets/unsubscribe
    messages/qos2/sent
    packets/pubrec/missed
    packets/pubcomp/sent
    packets/pingresp
    packets/pubrel/missed
    packets/puback/sent
    messages/received
    packets/pubcomp/missed
    packets/pubcomp/received
    packets/subscribe
    messages/retained

    clients/count
    clients/max
    retained/count
    retained/max
    routes/count
    routes/max
    sessions/count
    sessions/max
    subscribers/count
    subscribers/max
    subscriptions/count
    subscriptions/max
    topics/count
    topics/max


# Requirement

1.Eny version of Mqtt that uses management api v2

2.curl package on Mqtt host

3.Zabbix server v4.2 (probably works on other versions)

# Installation


1.Upload userparameter file to zabbix agent directory that is included in agent’s config file and restart agent.

2.Upload template file to zabbix server. Add template to host that has mqtt running.

3.Add these macros in host configuration:

{$MQTT_IP} => Mqtt server ip address

{$MQTT_PORT} => Mqtt running port

{$MQTT_USER} => Mqtt username

{$MQTT_PASS} => Mqtt password


After few moments you can see that items are getting values in Last data page.


I’m still wotking to imporve the template and create this template for other Mqtt versions.
