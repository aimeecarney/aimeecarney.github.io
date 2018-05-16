---
layout: post
title:      "React Application - SpotCheck"
date:       2018-05-16 21:17:16 +0000
permalink:  react_application_-_spotcheck
---


The day has finally arrived. I have submitted my final portfolio project for the Flatiron School. And I couldn’t be more proud of my final project.

Requirements:
* The code should be written in ES6 as much as possible
* Use the create-react-app generator to start your project.
* Follow the instructions on this repo to setup the generator: create-react-app
* Your app should have one HTML page to render your react-redux application
* There should be 2 container components
* There should be 5 stateless components
* There should be 3 routes
* The Application must make use of react-router and proper RESTful routing (should you choose to use react-router v3 please refer to the appropriate docs; docs for v4 can be found here)
* Use Redux middleware to respond to and modify state change
* Make use of async actions to send data to and receive data from a server
* Your Rails API should handle the data persistence. You should be using fetch() within your actions to GET and POST data from your API - do not use jQuery methods.
* Your client-side application should handle the display of data with minimal data manipulation
* Your application should have some minimal styling

I created an application where a user can input an address and the application will populate any permit parking zones in Chicago that may apply to that location.

This project was no easy feat. It being my final I wanted it to be something I was proud of and could brag about. This is an application that I had been thinking of ever since my Pay to Park app was “stolen”. You could say this was in rebuttal of that. It was created to help Chicago residents be confident in where they parked, without unexpected parking tickets. 

I first created my Rails API Backend which consists of two models: 1. Spot - which contains CRUD actions in the controller which the user can input. 2. Zone - which pulls from a third party API (the city of Chicago data portal) and assess the spot input and relays any permit zones near that address. From there I created my front-end react app through create-react-app. 

The biggest hurdle for me was using the react-redux middleware. While I still have much to learn about React-Redux, what I enjoyed most was the architecture, and the flow between the dispatch and actions. 

I plan on adding more features, I would like this to fetch the exact permit parking zone, rather than just listing zones that could apply. I would also like to pull more data from the city of Chicago, to let users know of any other parking restrictions that area might have. But for now I can sit back, relax and be proud of the past 15 months and confidently call myself a full stack web developer :) 

