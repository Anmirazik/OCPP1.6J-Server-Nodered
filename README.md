OCPP 1.6J Server
==========

OCPP 1.6 JSON developed using node-red and integrate with thingsboard through MQTT for Data Visualizations

Just a simple backend OCPP 1.6J prototype

### About

1. Just a simple OCPP 1.6J server prototype which I have developed using Nodered using this library https://github.com/Argonne-National-Laboratory/node-red-contrib-ocpp.git
2. It can receive ocpp commands from the charger such as BootNotifications, StartTransaction, StopTransaction and other basic OCPP commands
3. It also can send ocpp commands to the charger such as RemoteStartTransaction and RemoteStopTransaction
4. All the data received through OCPP protocol are then sent to thingsboard MQTT broker for Visualizations and controlling 

### Example Data Output

Below is an example of data output coming from the simulated ocpp charger where StartTransaction OCPP command is being sent from charger to the cloud  based on here https://github.com/vasyas/charger-simulator.git

```json
{
   "ocpp":{
      "chargeBoxIdentity":"OC",
      "MessageId":"cf988fc8-1f52-4aca-8f88-e4e5d199d779",
      "msgType":2,
      "command":"StartTransaction"
   },
   "_msgid":"36beaed13884a412",
   "payload":{
      "command":"StartTransaction",
      "data":{
         "connectorId":1,
         "idTag":"12345678",
         "timestamp":"2023-11-25T02:38:07.925Z",
         "meterStart":0
      }
   },
   "msgId":"8cd21349-c137-418e-aa6e-88d1d0e91d41"
}
```

### How the Integration With Thingsboard Looks Like 

#### Main Dashboard

So below is an overview of how the integration with Thingsboard looks like , just a simple dashboard to see the status of the charger

<img width="838" alt="image" src="https://github.com/Anmirazik/OCPP1.6J-Server-Nodered/assets/113960675/874f855c-705a-45b1-8643-0fba117eda77">

#### Session Dashboard

Below session dashboard shows the amount of energy consumptions for the charger and its individual transaction where it has the amount of power feed into the car and the price of each transaction

<img width="839" alt="image" src="https://github.com/Anmirazik/OCPP1.6J-Server-Nodered/assets/113960675/4be34ecd-66ed-428b-a1a3-7bb56275598f">




