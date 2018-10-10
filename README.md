## just a rough sketch of this readme
## take pictures and link them inline
## Add a link to this project in sandbox once complete

# Purpose
This is a guide on how to build and deploy a dockerized shiny app on Azure Container Registry with Web Service and CI/CD pipeline.

# Steps Overview

# Project directory organization
Docker works using Dockerfile, a file which specifies how Docker is supposed to build your application. 
It contains the steps Docker is supposed to follow to package your app. Once that is done, you can send
 this packaged app to anyone and they can run it on their system withno problems.

Let's start with the project structure. You will have to keep Dockerfile at the root of your project. A basic project will look as follows -

- app.py
- Dockerfile
- requirements.txt
- some_app_folder/
-   some_file
-   some_file

Dockerfile starts with a base image that decides on which image your app should be built upon. Basically "Images" are nothing but apps.
So for example you want your run your application in Rocker Shiny server 3.3.2 , you use rocker/shiny:3.3.2 as the base image.

# Build Shiny App
We begin by making our shiny app. You can do this in R by going to File> New File > Shiny Web App.
![ScreenShot1](shiny-app-screenshot.PNG)

# Dockerfile
Go deep on this, on what each command does and why.


## Base Images
Talk about FROM scratch option

## Installing libs
R and linux stuff

## Moving files into image

## Ports
There is a runtime docker build argument `-p 80:80' that needs to go here to map web port to container

# Azure Resource Groups
Overview and creation

# Azure Container Registry Service
setting this up

# Build Pipeline
config, build and push tasks, commit triggers on specific branches

# Web App Service
Docker container app option, you can test it live now before creating the release pipeline

# Release Pipeline
more config, remember to "unlink all", enable CD, set the trigger, specify the branch
