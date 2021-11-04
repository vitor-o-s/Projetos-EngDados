# The project

When you save the flow a link is generated and then you just make a POST to this link and the flow will be triggered.

Receiving the trigger, the flow reads the json received and generates variables in the next step, a personalized message will be sent on the Microsoft Teams channel.

* The json body is set manually in power automate
 
* In this specific case, POST was done via Azure DataFactory using a Web connector in the pipeline.

## Flow
![project flow](https://github.com/vitor-o-s/Projetos-EngDados/blob/main/MonitoringAndAlerts/Deactivationalert/powerautomate.png)


## JSON

In my case I only need to send/receive the table name

```json
{
    "properties": {
        "TableName": {
            "type": "string"
        }
    },
    "type": "object"
}
```
