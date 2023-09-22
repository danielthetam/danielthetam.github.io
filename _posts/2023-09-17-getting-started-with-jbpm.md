---
title: Getting Started with jBPM
categories: [Projects,  jBPM-qBPM]
date: 2023-09-16 15:00:00 +0800
---

## Starting the jBPM Server
Once we have installed jBPM and unzipped its contents, we can begin by navigating to the 'bin' folder and running 'standalone.bat'. This will get the jBPM server up and running. Once the server is up, navigate to Business Central("https://localhost:8080/business-central/") where we'll be met by the Business Central login page. 

## Getting started with Business Central
jBPM comes with a few default accounts for us to access, one of which includes our primary user, wbadmin, which we will use to log in to Business Central with the password, "wbadmin". By default, account passwords are the same as their usernames, with kie-server being an exception as it uses the password "kieserver1!". To access the list of accounts available to us, log in, and click on the cog icon on the top-right of the screen and click on users.

> In short, Business Central is a web-based application for users to implement, execute and monitor business processes. 

### Creating our Project
Now, we navigate to the Design tab and click on Projects. Next, add a new space named "MySpace", enter your new space, add a new project and name it "WFHRequest-Portal".
> #### Note: Follow the specified names
> Please follow the specified names because the application that we will be deploying later does in fact use these names. So make sure each name matches perfectly. 

Next, we'll begin adding assets into our project and developing it.