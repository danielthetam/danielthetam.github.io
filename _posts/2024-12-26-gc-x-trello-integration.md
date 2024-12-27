---
title: Google Classroom x Trello Integration App
categories: [Projects]
date: 2024-12-26 15:00:00 +0800
---
This documentation here is a tutorial on how you can set up the GCxTrelloIntegration app for your own personal use. This script was initially made for myself when we used Google Classroom for school assignments back in 2020. Now I have updated it following the changes in Google and Trello's protocol. 

> Feature requests can be sent to me through the "Contact" page on [my website].
> Feel free to build upon this script to make an actual Trello app that others can use.
> Google Classroom will be abbreviated as "GC" from now on.

# Prequisites
> * Python 3.10.7 or greater
> * pip package management tool
> 

# Getting your credentials.json file from Google
To start using the GC API, Google needs to some way of identifying the script/app that will be calling its services. So our first step should be to register our app and get the proper credentials.

First, create your own [Google Cloud project](https://console.cloud.google.com/). Then, enable its use of google's APIs and Services in the project menu. After doing that, follow the instructions in [here](https://developers.google.com/classroom/quickstart/python) starting from "Enable the API" up to "Install the Google client library". 
> Make sure to save the 'credentials.json' file

Then, download the [project files](https://github.com/danielthetam/GCxTrelloIntegration) from my GitHub, and store it in a dedicated project directory. 
Next, move the 'credentials.json' file to the project directory.

# Integrating trello
In our script, we used py-trello, a wrapper for Trello's REST service. Just like our GC API, we now need to register our app to use the API. First, navigate to Trello's [Power-Ups & Integrations page](https://trello.com/power-ups/admin). Create a new integration and fill in the details. You can leave the iframe connector field empty. 

After creating it, you should be prompted with the option to generate a new API key. You will then be shown your API key and secret after generation. Next, go to the project directory and edit the ".env" file. Replace the strings with your corresponding API key and secret. Go back to Trello, navigate to the "API key" tab. To the right, there should be a wall of text. Click on the link to generate a token. Click "Allow", and you will be given a token.

> Your tokens and API keys should all be kept private. Do not share them with others.
Then, replace the string in the ".env" file with your token. 

Next, run "quickstart.py". You should then be redirected to a page for manual authorisation of the app. Ensure you authorise using the Google account that is a member of the class you are trying to pull your assignments from. 

> If you have any permission error, head over to your Google Cloud project, and edit the permission scopes to allow the app to access all coursework.

[//]: # ()
   [my website]: <https://danieltam.com/>
