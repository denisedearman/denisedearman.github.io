---
layout: post
title:  "My Rails App"
date:   2017-08-25 20:25:24 +0000
---


Today I am finishing up my rails application project. I have called it Blendspiration because it is a recipe app for smoothies to give users inspiration for their next smoothie!



# My approach
My approach to this project was to first sketch out my models and how they would be associated. For this project I had four models: Users, Recipes, RecipeIngredients, and Ingredients. The RecipeIngredients model was my join table that also included the units (tablespoons, cups, etc) and quantity. Each user has many recipes. Recipes belong to users, have many recipeingredients and have many ingredients through recipeingredients. RecipeIngredients belong to a recipe and belong to an ingredient. Ingredients have many recipeingredients and many recipes through ingredients.


I also added some validations to each of my models as I created them. Most of the validations were uniqueness and presence constraints, but I also added that quantity for recipe ingredients needed to be greater than 0 and that units needed to be within a list of different units.


After the models, associations, and validations were created I went on to making some of the forms. I basic view forms and new forms for the models using partials.


I had some trouble with creating the recipe form because I needed to essentially create a new recipe_ingredient with each new recipe. I ended up figuring this out and needed to use a custom attributes method in my recipe model (recipe_ingredients_attributes=) to get this to work. To keep the app simple I do not allow users to create a new ingredient on this form also. For now the user needs to select ingredients via a drop down list.


For my class method requirement I created a "simple_recipes" method in my recipe class that returns all recipes with 5 or less ingredients. I made a custom route to /recipes/simple-recipes so that users could view this page.


Now I am adding the final touches and styling the app slightly (I couldn't resist!).



