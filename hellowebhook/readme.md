# Hello Webhook

This example guides you on getting started with built.io and a simple webhook. This shows how to setup an rest api endpoint in builtio (webhook) and output an email when the api is accessed, which can be easily accomplished with a simple GET request from Curl or Postman. 

## Setup

1. Create a new, 'Blank Workflow' by selecting the plus sign at [built.io flow](https://flow.built.io). You should see a empty canvas with a green start and a red stop icon. These are the starting and stopping points of the flow. ![initial](https://github.com/SoftwareAG/builtio-examples/blob/master/hellowebhook/initial.PNG)

 
2. The Webhook is created by modifying the start icon, which is is the entrypoint to the new flow. Please select the gear on top of the start icon to access settings. Once settings is selected in the start icon, a 'trigger' dialog will appear that allows Webhook to be selected.![step1](https://github.com/SoftwareAG/builtio-examples/blob/master/hellowebhook/step1.PNG)


3. Leave Webhook Authentication and Webhook Payload unchecked for now and hit next. Feel free to modify these if desired, they are easy to return to and iterate as well. At the very least, Authentication should be added immedately after 'Hello world' is working. Note the webhook url and save this for later. ![webhook-config](https://github.com/SoftwareAG/builtio-examples/blob/master/hellowebhook/1-webhookconfig.png)


4. Select done once presented with the final dialog. You should now see the start arrow dialog replaced with a webhook icon. ![webhook-2](https://github.com/SoftwareAG/builtio-examples/blob/master/hellowebhook/2-webhook.PNG)


5. Now lets have the flow do something once the webhook receives a request. Search in the search dialog for 'email' and find the 'Send an Email' notification. ![send-email](https://github.com/SoftwareAG/builtio-examples/blob/master/hellowebhook/sendemail.PNG)


6. Select the 'Send an Email' and drag it between the start and end icons. Connect the arrows from start to the email icon and then to the end icon. This inserts the 'Send an Email' step in the flow. ![send-emailicon](https://github.com/SoftwareAG/builtio-examples/blob/master/hellowebhook/sendemailicon.PNG)


7. Next, select the settings icon at the top of 'Send an Email' and enter in a friendly email address. ![email-addy](https://github.com/SoftwareAG/builtio-examples/blob/master/hellowebhook/emailaddy.PNG)  


8. Select the green arrow at the top right. This 'saves' the workflow and enables testing. You should see a testing popup. ![green-arrow](https://github.com/SoftwareAG/builtio-examples/blob/master/hellowebhook/greenarrow.PNG)  


9. Now, everything should be ready to go. Send off a quick curl command (or use postman/method of choice) to the webhook url given earlier in step 3. This url is custom to your project and can be accessed by selecting the gear icon in the webhook start icon. 
![webhook-config](https://github.com/SoftwareAG/builtio-examples/blob/master/hellowebhook/1-webhookconfig.png)


Curl command example

```
curl https://runflow.built.io/run/abcd1234
```

If all goes well, you will see something similiar

```
{"message":"Workflow enqueued successfully.","code":123,"bill_uid":"123123123123123","flow_uid":"1231231234","user_uid":"123123123"}
```

## Troubleshooting

1. If you get this error

```
{"error":"Parameters missing. Please provide all required parameters in actions before running workflow","code":126}
```

It could mean the flow isn't saved yet. Make sure the green arrow in the top right is checked and the flow is enabled. 
