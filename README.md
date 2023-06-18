# Recipe Hero

![Recipe Hero example](recipe-hero.jpg)

Refactor the HTML and CSS in `src/App.js` to use components and dynamically filter data.

* Your solution should have over 7 components
* Replace all hard-coded data with dynamically fetched data from the `recipes.json` file in the `public` folder
* The ingredients should be generated dynamically
* As ingredients are added from the list, the list of available recipes should filter in real time
* Recipe step navigation should be functional
* There should be a default message displayed if no recipes match the selected ingredients

## Rubric

* [ ] - Code has over 7 components
* [ ] - No hard-coded data, including ingredients
* [ ] - Recipes are fetched from JSON file
* [ ] - Adding and removing ingredients changes the available recipes
* [ ] - Multi-step Recipes can navigate forward and backward
* [ ] - Having no recipe matches displays a useful message
* [ ] - Styling is preserved


## Notes

1. Get the data from the recipes.json 
2. Curate an array of unqiue ingredients from all of the recipe ideas -- essentially show them the available items to select from
    - component to copy the existing list and remove via filter the ones selected 
    - function to add to #3
3. New array to show the existing of ingredients selected
    -  function to delete a selected ingredient
4. show list of recipes that have each of the selected ingredients

```js
selectedIngredients.every(recipe.ingredients.includes) // should return a boolean of true if it includes it

recipes.filter(^^)  // filter the list for scenario 2 & 3

if array.length === 0, show error message, else do 4
```

- scenario 1: if nothing matches all selected ingredients >> error message 
- scenario 2: if no ingredients are selected >> all recipes 
- scenario 3: updates as you add ingredients / renders recicpes that apply

5.
6. 
7. Next button will use useState to then `nav + 1`, previous button will be `nav - 1`
8. if `nav > 1`, show previous | if nav < recipe.steps[recipes.step.length-1].stepNumber,  show next