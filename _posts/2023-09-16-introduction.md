---
title: Introduction
categories: [Projects,  jBPM-qBPM]
date: 2023-09-16 15:00:00 +0800
---
> #### Disclaimer
> I am by no means a professional on the topics mentioned nor the technologies, rather, this documentation is a blog on my experience as an amateur
> and hopefully serves as a light in the dark for beginners or any curious developers looking to perform a little project with business automation.

## What is jBPM?
[jBPM] is a business automation tool for automating business processes with ease, and providing accessibility through REST APIs and comprehensive documentation for said APIs. Optionally, with jBPM as a foundation, we can also build our own powerful applications and tools to personalise our experience, one of which includes [qBPM].

## What is qBPM?
[qBPM] is a demonstrative web application for showcasing how [jBPM] can be used to create powerful tools through smooth integrations with various open source technologies. 

## Purpose of this Documentation
This documentation will be dedicated to walking you through how you can set up a [jBPM] server, customise it to fit our needs, utilise [jBPM] to create automated processes, and integrate them with [qBPM], our own custom webapp for presenting these automated processes.

## What will we be creating in this walkthrough?
We will be using jBPM to create a work from home request portal to automate the process of requesting to work from home. This will help ease the lives of our HR team as well as employees.

## Prerequisites
* [Installation of jBPM Server Distribution](https://www.jbpm.org/download/community.html)
* [Node.js LTS](https://nodejs.org/en/download)
* [Postgres](https://www.postgresql.org/download/)
* [JDK 17](https://www.oracle.com/uk/java/technologies/downloads/#jdk17-windows)
* [Stable version of Apache Maven](https://maven.apache.org/download.cgi)
* [Visual Studio Code](https://code.visualstudio.com/download)

> #### Note
> Every process mentioned in this documentation is based on my experience in Windows 10, so do keep in mind that results may vary from operating system to operating system

[//]: # ()
   [jBPM]: <https://jbpm.org>
   [qBPM]: <https://github.com/danielthetam/qBPM>