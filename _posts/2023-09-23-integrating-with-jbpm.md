---
title: Integrating with jBPM
categories: [Projects,  jBPM-qBPM]
date: 2023-09-16 15:30:00 +0800
---

## Setting up our Postgres database
Open your Postgres setup, and just step through everything while following the default configurations, but ensure that you note down your password and your host, and also make sure that `Command Line Tools` is ticked as an installation configuration.

After installation, search for `psql` in your search bar and open the application. Once you open it, you'll see something like this: `Server [localhost]:`, we can just hit enter until we get to `Password for user xxx:` where you have to type the password you noted down during the setup.

Once you have logged in, we can go ahead and create a new database by typing `CREATE DATABASE qbpm;`. Ensure you put a semi-colon after every statement because it marks the end of a statement in SQL(Structured Query Language).

## Configuring SpringBoot's application properties
Now, we shall set up qBPM. Go ahead and download or clone this [GitHub repository](https://github.com/danielthetam/qBPM). Once you have downloaded it, navigate to `API\src\main\resources\application.properties` and edit it with any simple text editor.

**If you have prior experience in Postgres and did not follow the steps above**, change the value of `spring.datasource.url` to this `jdbc:postgresql://host:port/database` where you change the values `host`, `port`, `database` with the appropriate details. If you have been following the default values and the steps above, you can leave it as is.

Next, change the value of `spring.datasource.username` to your user account(by default it is `postgres`), and change the value of `sprng.datasource.password` to the password you noted down.

## Running qBPM
### Running the SpringBoot API
Now, open Visual Studio Code, head to the top menu bar, click on File > Open Folder and navigate to the `API` folder and open it. Then, click on the Extension button(4x4 cube with a detached top-right cube) on the left menu bar, and search for the extension `Spring Extension Pack`. This will download all the required extensions to run our application. After installation, navigate to the top menu bar again and click on Terminal > New Terminal. Then, in your terminal, enter `& 'C:\Program Files\Java\jdk-17\bin\java.exe' '-cp' 'C:\Users\yourusername\AppData\Local\Temp\cp_2e9afgjm2aisca0ev8fztta4w.jar' 'com.daniel.qbpm.qBPMApplication'`. Ensure that you change `yourusername` to your username. 

### Running the React API
Now, go to File > New Window. In the new window, repeat the same step to open a folder but open the `react-view` folder instead. Then, open a new terminal, enter the command `npm install`, and npm(node package manager) will install all the required packages for you. After it is done, enter the command `npm start` to start the React application. Then, open `https://localhost:3000` to access the app. 