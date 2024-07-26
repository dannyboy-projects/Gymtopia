# Gymtopia
The Best Gym and Nutrition spreadsheet

First, Gymptopia allows users to input body weight, body fat % (BF%), physical dimensions, and personal bests across a number of lifts in order to 
track progress. 

Second, an ingredients database where macros per 100 g are stored has been created and can be added to dynamically. Similarly for recipes, a database of
recipes has been created, allowing for weekly macros to be projected and nutrition targets to be set. 


## Features

(1) PB lift tracker<br>
(2) Golden Ratio dimension calculator and tracker<br>
(3) Weight and BF% Tracker<br>
(4) Ingredients Database <br>
(5) Recipe Database <br>
(6) Weekly Macros Planner <br> 

## How to Use

- **Data Entry**
  - A: Muscular Dimensions, records current proportions to 'Physical Dimension DB' and calculates Golden Ratio dimensions based on non-domninat wrist, knee circumference, waist circumference (https://legionathletics.com/ideal-male-body/)
  - B: Weight, simply records current weight to the 'Weight DB'
  - C: BF%, records body fat % to 'BF% DB'
  - D: Personal Best, records PB  on important lifts to "Lifts PB DB'. Note that one PB or many can be recorded at the smae with the same or different dates without issue
 
- ** Ingredients List
  - Macros per 100 g are added manually to list (protein, fat, carbs, kcal, cost)
  - This list is reaad dynamically by the `=INGREDIENT_LIST()` custom VBA function

- ** Recipe Library
  - Create a new recipe by copying and pasting the top two rows of the previos recipe, place the new recipe below with one blank row spacing
  - To add a new ingredient copy and paste columns C:K and paste below, if needed retype `=INGREDIENT_LIST()' in column C to refresh
  - Note the summary total in columns O:S will refresh automatically
  - Give the new recipe a name and all recipe names on this page are dyanmically read by the `=RECIPES_LIST()` custom function

- ## 7-day Meal Plan
  - Start by entering your body weight, age, height and slecting an activity factor in cell C5
  - A BMR will be calculated according to the Mifflin St. Joer equation for Men - in order to adjust the calcualtion for Women, change the first term to G8 (Female offset) (https://www.ptpioneer.com/total-daily-energy-expenditure-calculator-tdee-calculator/#:~:text=chosen%20activity%20level.-,The%20Mifflin%20St.,%2D161%20(kcal%20%2F%20day)
  - Next Selcet an activity factor from the drop down menu in C6, leading to a Total Daily Energy Expenditure (TDEE) estimate in cell C7
  - In each blue cell `=RECIPE_LIST()` will have to re-entered in order access the most up to date recipe list
  - Essentially, the macros from the Recipe Library are aggregated here, and it is possibel to plan your weekly macros
  - The top right hand corner estimates the quantity of protein intake based on 0.7g/lb of body weight
  - Fat intake in calculated as 20% of TDEE with fat accounting for 9 kcal/g - an estimate of daily fat intake (g) is shown in cell N4
  - The remaining calories are assign to carbs in cell N3
  - Set target surplus/deficit depending on gym goal (Bulk = 200 - 500 kcal surplus / Cut = 100-300 kcal deficit / Recomp = 100 - 150 kcal deficit whilst maintaining protein and resitsance training)
  - Happy planning your weekly macros targets!







