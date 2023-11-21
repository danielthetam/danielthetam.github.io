---
title: Preparation for jBPM integration
categories: [Projects,  jBPM-qBPM]
date: 2023-09-16 15:30:00 +0800
---

## How does integration work?
As previously mentioned, jBPM allows for smooth integration with its accesible and well-secured REST API. It enables us to create our own powerful tools that act as an extension of jBPM, an example of such is the one I've created for demonstrative purposes, qBPM. 

Before we begin, we need to understand the structure of qBPM. qBPM uses a React frontend and a SpringBoot backend. Aside from serving as our React application's API, SpringBoot serves as a proxy between jBPM and our client-side due to browser CORS policies preventing us from sending requests to jBPM(at least for me) through our React application. Besides, I find it more organised to have my client application only call from a single domain and have my backend do most of the dirty work. 

## Configuring jBPM
Before we begin downloading the codebase and setting things up, we need to configure our jBPM's system settings. As previously mentioned, jBPM's REST API requires authentication to access it. That's why we use `wbadmin` as our system admin account and use its credentials for authentication. 

However, when we want to get tasks specific to a user, let's name them User B, by default it only returns tasks that are available for the user that we use for authentication(i.e wbadmin's tasks). In order to get the tasks for User B while using `wbadmin`'s credentials instead of User B's credentials, we need to enable bypass authentication in jBPM's configuration. 

> We can't use User B's credentials because qBPM ensures that passwords are [hashed](https://www.okta.com/blog/2019/03/what-are-salted-passwords-and-password-hashing/#:~:text=Password%20hashing%20is%20defined%20as,unintelligible%20to%20the%20bad%20actor)

Let's get straight to that. Navigate to jBPM's root folder, enter the `standalone` folder, enter `configuration`, and edit `standalone.xml`. Under the `<system-properties>` tag, add the line: `<property name="org.kie.server.bypass.auth.user" value="true"/>`. Save it, and restart jBPM.
