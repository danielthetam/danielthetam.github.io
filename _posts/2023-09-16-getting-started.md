---
title: Getting Started
categories: [Projects,  jBPM-qBPM]
date: 2023-09-16 15:30:00 +0800
---

## Starting the jBPM Server
Once we have installed jBPM and unzipped its contents, we can begin by navigating to the 'bin' folder and running 'standalone.bat'. This will get the jBPM server up and running. Once the server is up, navigate to Business Central("https://localhost:8080/business-central/") where we'll be met by the Business Central login page. 

## Getting started with Business Central
jBPM comes with a few default accounts for us to access, one of which includes our primary user, wbadmin, which we will use to log in to Business Central with the password, "wbadmin". By default, account passwords are the same as their usernames, except for kie-server, which uses the password "kieserver1!". To access the list of accounts available to us, click on the cog icon on the top right of the screen and click on users.

> In short, Business Central is a web-based application for users to implement, execute and monitor business processes. 

### Creating our Project
Now, we navigate to the Design tab and click on Projects. Next, add a new space named "MySpace", enter your new space, add a new project and name it "WFHRequest-Portal".
> #### Note: Follow the specified names
> Please follow the specified names because the application that we will be deploying later does in fact use these names. So make sure each name matches perfectly. 

### Creating Data Objects
Now, we will begin adding our assets. First, let's clarify what objects we'd need for our request portal. The best way to do this is to visualise our process by creating a scenario and analysing it. 

In our portal, we'll have an actor who submits a request, groups of actors who process the request and a final actor who decides whether the request is approved or not. Ultimately, all of these actors are employees, so that can be declared as an object of itself. Then, we also have the request object, which should contain information about the request made by the first actor.

#### Employee Data Object
Now, let's add a Data Object(which are underlyingly Java object classes with fields you can define) named Employee and package it under "com.myspace.wfhrequest_portal". Let's add some fields which define the attributes of each employee.

##### Add the fields:
* Identifier: `eid`
    * Label: `Employee ID`
    * Type: `Long`
* Identifier: `email`
    * Label: `Email`
    * Type: `String`
* Identifier: `name`
    * Label: `Name`
    * Type: `String`

We then save the object by clicking on "Save".

#### Request Data Object
We'll add another Data Object named Request, and package it under "com.myspace.wfhrequest_portal". Now, we'll define the attributes for our Request object.

##### Add the fields:
* Identifier: `numOfDays`
    * Label: `Number of Days`
    * Type: `Integer`
* Identifier: `reason`
    * Label: `Reason`
    * Type: `String`
* Identifier: `reqDt`
    * Label: `Rq Dt`
    * Type: `Integer`

`numOfDays` represents the number of days the employee will be working from home, starting on reqDt(the requested date). `reason` represents the reason for the request. Once again we save the object.

### Defining our business process
Now, we design the business process and define its flow. 