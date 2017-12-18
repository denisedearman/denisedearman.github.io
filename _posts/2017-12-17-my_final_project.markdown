---
layout: post
title:      "My Final Project"
date:       2017-12-18 01:04:21 +0000
permalink:  my_final_project
---


The time has come!

After starting a new job at the end of September I had to put my progress in FIS on hold for some time. There are only so many hours in a day and so many hours in a day that I can be learning new things. I was able to finish the curriculm shortly before starting my job so I have only had my final project left for months. 

I am happy to have now completed the requirements for the final project after spending most of some my weekends working on this!


For my final project I chose to create a react version of an Italian card game that I learned in college called Scopa. It's a very fun game with a little bit complex rules. To limit the scope of my project I decided to do a pass and play 2 player version of the game.


As usual I started off by figuring out my models. I had to make some adjustments along the way but my basic idea worked for the most part. 

I have games which have many player_games and many players through player_games. A game also has many cards. 
Cards belong to games and belong (optionally to a player_game). Originally I had that cards optionally belonged to a player. But I soon realized that this made everything way more difficult for querying and so I made this a player_games association instead.

I decided to create a separate rails project that would proxy on 3001. Then my react project calls out to this api. 

The react portion I ended up with 10 containers and 5 components. I have 7(!) reducers.

The basic flow of my application is that from any page the user can choose to view the about page, view all players, create a new game, or view all games.

From the create a new game the user can submit the names of 2 players that they want to match up together. This then takes them to the game show page. The game show page has a button to "Start" the game. Then the start always makes a call to the backend to figure out whose turn it is or if its a new game to deal out the cards ('/games/:id/play').

This will take the user to /games/:id/players/:id which will say "{name} its your turn!" and have a play button.  I made this page to make there be a screen always ahead of a move for the pass and play minimal security :) 

When the user hits to take their turn they are directed to /games/:id/payers/:id/edit. Essentially the user is editing a player when they make their move (although they may also be altering the game through the player. The turn page will not allow a user to make a bad move but it could use some updating and refining with giving a message etc. When the player makes their move it will take them to the landing page for the next player's turn.


At the end of the round of the game there will be a link to view the summary of the round. This takes the user to /games/:id/summary. This summary gives a generic view of how the game was scored and shows all the captured cards of each player and the ending table state.


I would like to continue updating the game by adding pictures instead of text for the cards, adding error messages, adding suggested moves, and adding more playing options including a computer player and more than 2 person game.

But for now I am so happy to have reached this milestone!!!!!




