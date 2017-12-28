# EDI X12 270 Processing Example
This is a project that demonstrates processing an X12 270 message using MuleSoft Anypoint B2B

## Application Flow
The diagram below shows the flow of the application and how it interacts with Anypoint MQ.

<img src="https://github.com/djuang1/mulesoft-edi-x12-270-processing/blob/master/assets/x12-270-processing.png" width="500px">

## Setup
1. Create Client App in MQ and copy down the client ID and client secret
2. Create an exchange called <b>DemoExchange</b>
3. Create 3 queues
  * <b>DemoDLQ</b>
  * <b>DemoQueue</b> - Assign <b>DemoDLQ</b> as the Dead Letter Queue for this queue.
  * <b>ErrorQueue</b> - Assign <b>DemoDLQ</b> as the Dead Letter Queue for this queue and set the 'Delivery attempts before reroute' to 1
4. Edit the <b>DemoExchange</b> and bind the <b>ErrorQueue</b> and the <b>DemoQueue</b>
5. Edit the <b>mule-app.properties</b> file in the imported Mule project in Studio and populate the properties.
6. Run the project in Studio
7. Open a browser and open the following URL to kick off the flow - http://localhost:8081/test?number=123
