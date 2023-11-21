---
title: Creating Data Objects and Groups
categories: [Projects,  jBPM-qBPM]
date: 2023-09-16 15:00:00 +0800
---

## Creating Data Objects
Now, we will begin adding our assets. First, let's clarify what objects we'd need for our request portal. The best way to do this is to visualise our process by creating a scenario and analysing it. 

In our portal, we'll have an actor who submits a request, groups of actors who process the request and a final actor who decides whether the request is approved or not. Ultimately, all of these actors are employees, so that can be declared as an object in and of itself. Then, we also have the request object, which should contain information about the request made by the first actor.

### Employee Data Object
Now, let's add a Data Object(which are underlyingly Java object classes with fields you can define) named Employee and package it under "com.myspace.wfhrequest_portal". Let's add some fields which define the attributes of each employee.

#### Add the fields:
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

### Request Data Object
We'll add another Data Object named Request, and package it under "com.myspace.wfhrequest_portal". Now, we'll define the attributes for our Request object.

#### Add the fields:
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

## Creating our groups
In jBPM, we have what we call groups. Groups enable us to organise users into their respective teams and/or departments. In our scenario, the groups who process the request can be broken down into two separate groups of actors. For now, that's all we have to know. 

Let's create the groups by clicking on the cog icon on the top-right corner and clicking on "Groups". Click "New Group" and name it "HR" for Human Resources. Then, we will be prompted to assign users to that group. We can just assign ourselves to the group. Next, repeat the same step but name the group "ManualFilters".
