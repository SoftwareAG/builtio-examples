# Salesforce -> Slack Webhook

This example guides you on getting started with built.io and a straight forward integration between Salesforce and Slack. This tool enables you to stand up a basic integration in approx 5-10 minutes, giving you a working connection that you can then add additional features. Alternatively, implementing this connection by hand can take hours or even a day or two if you are unfamilar with the Slack or Saleforce api. 

Within built.io, there are hundreds of already developed flows in a library. These are straight forward to get started with. 

## Setup

1. In the default workflows dialog, begin by selecting 'Add From Library' to create a new flow from an existing template. ![library](https://github.com/SoftwareAG/builtio-examples/blob/master/salesforceslack/library.PNG)

2. Type in Slack and find the Salesforce + Slack integration. This was on the sixth page at the time of the writing of this tutorial. ![salesforceslack](https://github.com/SoftwareAG/builtio-examples/blob/master/salesforceslack/salesforceslack.PNG)

3. Once selected, you will be prompted to configure the Salesforce connection. This is straight forward and can be accomplished with a few clicks via an OAuth flow. Built.io will access the leads from Salesforce using your credentials when you grant access. Make sure to select the 'test' button once the access is authorized to verify functionality. A quick 'success' response will provide confidence to move forward with the next step, otherwise troubleshoot the OAuth. ![salesforceslack-2](https://github.com/SoftwareAG/builtio-examples/blob/master/salesforceslack/salesforceslack-2.PNG)

4. The next step is to configure the Slack connection as well. The is also a simple OAuth enablement. Once its working you can go in and configure a bot user, until you do so any Slack messages will be posted as your account. You will need to choose a valid private or public room in Slack for the destination message. Again, it is helpful to test before continuing. ![salesforceslack-3](https://github.com/SoftwareAG/builtio-examples/blob/master/salesforceslack/salesforceslack-3.PNG)
 ![salesforceslack-oauth2](https://github.com/SoftwareAG/builtio-examples/blob/master/salesforceslack/salesforceslack-oauth2.PNG)

5. Now the flow is established, assuming each component is tested and working the entire flow should be ready. Create a new lead in Salesforce and watch the message arrive in Slack! ![salesforceslack-5](https://github.com/SoftwareAG/builtio-examples/blob/master/salesforceslack/salesforceslack-5.PNG)

## Bonus

1. Additional Salesforce Triggers: Now that the flow is established, alternate alerts from Salesforce are straightforward. Select the settings gear on the Salesforce icon and browse the trigger label dialog. Other triggers such as 'New Opportunity' and 'New Task' are easily selectable as well. 
![salesforceslack-6](https://github.com/SoftwareAG/builtio-examples/blob/master/salesforceslack/salesforceslack-6.PNG)


2. Additional Imported Slack Fields: Additional fields can be imported to Slack from Salesforce. The potential fields can be browsed by copying the $Trigger keyword and entering in the . after it. This will initiate a popup dialog with all the potential imported fields. For example 
```
Description: {{$trigger.
```
![salesforceslack-7](https://github.com/SoftwareAG/builtio-examples/blob/master/salesforceslack/salesforceslack-7.PNG)
