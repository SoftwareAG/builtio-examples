# Hello Webhook

This example guides you on logging data to the browser console in built.io. It also introduces the capability to write node.js code within the browser, greatly extending the use-cases for the tool. 

## Setup

1. Start by converting the start icon into a webhook. If you are unfamiliar with this step, please complete it by completing the first four steps in [hellowebhook](https://github.com/SoftwareAG/builtio-examples/tree/master/hellowebhook). When completed, your screen should look like ![webhook-2](https://github.com/SoftwareAG/builtio-examples/blob/master/hellowebhook/2-webhook.PNG)

2. Next drag over the Node.js icon under 'Developer Tools' on the right hand side. I found it easier to search for 'Developer' in the right nav. Keep the default code in the Node.js settings, which at the time of this writing is '$export(null, { done : false });'. We are going to log this in the next step. Select complete and save. ![Nodejs](https://github.com/SoftwareAG/builtio-examples/blob/master/helloconsole/addnodejs.PNG)

3. Now drag over a Logger icon under 'Developer Tools' on the right hand side. Connect the Nodejs icon to the logger. ![Logger](https://github.com/SoftwareAG/builtio-examples/blob/master/helloconsole/addlogger.PNG)

4. Next select the gear on the Logger icon to config the Logger. Expand the node.js Code on the right until the variable done=true is visible under output. Drag this variable to the left under 'Log Data' to enable logging the variable when the workflow is triggered. ![loggerconfig](https://github.com/SoftwareAG/builtio-examples/blob/master/helloconsole/loggerconfig.PNG)

5. Finally, trigger the workflow and observe the console which is logging the variable output from the node.js step. This is a good way to get quick feedback when using developer tools and in particular node.js within the tool. This is a good foundation to build upon for more sophisticated flows. ![finalstep](https://github.com/SoftwareAG/builtio-examples/blob/master/helloconsole/finalstep.PNG)
