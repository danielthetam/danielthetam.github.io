---
title: Deploying our Business Process
categories: [Projects,  jBPM-qBPM]
date: 2023-09-16 14:56:00 +0800
---
## Deploying our project
Before we deploy our project, we need to generate the forms required for our process. To do this, head into our `request-portal` process, click on the form button(form icon to the left of the Download button), and click `Generate all forms`. This will generate all dedicated forms for our business process. Once generated, we should see some new form assets in our project. 

Now, head over to the form named `WFHRequest-Portal.request-portal-taskform`. This is our main process form and is what is shown to the employee who starts the process instance to submit a request. By default, the form generates fields for all process variables, but we only want the employee to fill up the `employee` and `request` process variables. Therefore, we may remove all other fields besides the mentioned two by clicking on the vertical ellipsis icon and clicking remove.

Once complete, we can exit to the project explorer and hit `Deploy` to deploy our project. 

## Testing our project
Once the project has finished building, you can click the Menu button and click on the process definition tab. Click on the vertical ellipsis beside our `request-portal` process definition, and click start to create a new process instance. Next, fill in the form details. 

Now, click on the Menu again and click on the Task Inbox. Through there, you can access user tasks assigned to you or your group. You may then monitor the progression of each process instance and their details by clicking on Menu, clicking on Process Instances and clicking into your desired instance. 
