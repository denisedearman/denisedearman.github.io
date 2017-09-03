---
layout: post
title:  "My jQuery Project"
date:   2017-09-03 23:32:52 +0000
---


Today I just finished up my jQuery fronend Rails project. This project was a little bit easier as far as designing went because it was basically a build upon the Rails project. I managed to make my Rails project (mostly) a single page app!


# Project Process
For this project I started by transferring my indexes into a single page app with the home page. I added two containers to my home page "mainTitle" and "mainContent" that I decided would be my containers that would change. Getting the indexes to use JSON responses was fairly simple. First I added and tested my serializers. This took a little bit of trial and error because of my relation between Recipes and Ingredients through RecipeIngredients.

After getting the serializers correct I added a couple of Javascript functions. The first I setup to have an event listener on the Recipe Index button. When clicked the listener calls my displayRecipeIndex method. This method uses a jQuery call to the GET /recipes route. I changed the recipes controller to render a JSON response for this request. Then, in the displayRecipeIndex method I call another method on each JSON recipe in the JSON response. Once my recipes index was correctly displaying single page I did a similar process for the ingredients index.

Having completed the index display I decided to move onto the show pages. For these I added an even listener on the buttons in each index to call a loadRecipe(recipe_id) or loadIngredient(ingredient_id) javascript method. This method changes the title and content to be of the specific id called by making a GET /recipes/:id or GET/ingredients/:id call.


Finally, I worked on adding JSON model objects for recipes and ingredients and getting my create pages working. For each of the forms I created a Handlebars template. For the recipe form I pass a JSON object to setup the 10 possible recipe ingredients and populate the drop down lists. Then I setup the createRecipe() or createIngredient() method to be the submitAction for the template. In the create method I make an AJAX call to the post '/recipes' or '/ingredients' route. On success I create a JSON model object and display a template of the create object.

