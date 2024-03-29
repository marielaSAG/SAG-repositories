# Use GET HTTP Method to request data from a specified resource and send an email with the content

This example shows how to send an email to respective audience with requested data from a specified resource. 

We use this example to remind our moderators once a week for unanswered topics in [TECHforums](https://tech.forums.softwareag.com/). In Discourse platform such functionality is missing and using webmethods.io for creating it turned out to be much easier than creating a Discourse plugin..

## Setup

1.  Go ahead and get started creating a blank workflow. If you need a refresher on how to get to this point, this [guide](https://docs.webmethods.io/integration/workflow_building_blocks/creating_first_workflow/#gsc.tab=0) can be a great introduction. 

2.  If you want the email to be sent periodically, you can do this by using polling triggers. In this example we will use Clock trigger and set an email to be send every week. Click on the small setting icon on start step and choose Clock trigger. Use the edit option to choose day and time and click Done.<br/>![image](https://user-images.githubusercontent.com/45091718/126774332-8decea87-297b-49f4-ba3f-7d771462ca42.png)

3.  Add the HTTP Request service in the canvas by drag and drop feature. This automatically connects with the Clock trigger.<br/>![image](images/ConnectHTTPRequest.png?raw=true)

4.  Click on the small settings icon on the HTTP Request service  to select HTTP Method and add an URL.<br/>![image](https://github.com/SoftwareAG/webmethodsio-examples/blob/master/httprequest-sendemail/HTTPRequest.png?raw=true)

5.  To create custom HTML email template use Node.js service and add it in the canvas by drag and drop feature. Connect it to HTTP Request service.<br/>![image](https://github.com/SoftwareAG/webmethodsio-examples/blob/master/httprequest-sendemail/Nodejs.png)  ![image](https://github.com/marielaSAG/SAG-repositories/blob/master/images/ConnectHTTPRequest.png)

6.  We have a cool feature which is sending email where you can send the content to respective audience. Search for "send an email" and drag and drop the "Send an Email" service to canvas.

7.  Map the required fields in the Send an Email service. In this example we have mapped the address, subject and body.

8.  This completes the workflow and connects to stop step.<br/>![image](https://github.com/SoftwareAG/webmethodsio-examples/blob/master/httprequest-sendemail/FinalWorkflow.png)

9.  Check the email to review the results of the workflow.

```
testing code 
```

Testing `more inline code`

And some links [GitHub](http://github.com)

    > nvm use 8.14.0

    > wmio -v

    > wmio login #Enter the required parameters like your tenant, email and developer key. 

    > wmio init #Enter the name of your connector
    
Some table tests

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

Bullet test

* Start a line with a star
* Profit!

## This is a title tag
