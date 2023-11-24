ocppserver
==========

OCPP 1.6 JSON developed using node-red and integrate with thingsboard through MQTT for Data Visualizations

Just a simple backend OCPP 1.6J prototype

### About

1. Just a simple OCPP 1.6J server prototype which I have developed using Nodered using this library https://github.com/Argonne-National-Laboratory/node-red-contrib-ocpp.git
2. It can receive ocpp commands from the charger such as BootNotifications, StartTransaction, StopTransaction and other basic OCPP commands
3. It also can send ocpp commands to the charger such as RemoteStartTransaction
4. All the data received through OCPP protocol are then sent to thingsboard MQTT broker for Visualizations and controlling 