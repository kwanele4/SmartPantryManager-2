# Smart Pantry Manager

A Java Android application developed for Mobile App Development 700.

## Description
Smart Pantry Manager helps users keep track of ingredients in their pantry and suggests recipes only when all required ingredients are available in the required quantities.

## Main Features
- Add, view, edit and delete pantry ingredients.
- Store ingredient name, quantity, unit and optional expiry date.
- Display pantry data using RecyclerView.
- SQLite persistent local database.
- 20 seeded recipes.
- Strict recipe matching.
- Simple singular/plural normalisation.
- Unit compatibility checking.
- Recipe detail screen with ingredients and preparation steps.
- Settings screen.
- Feedback when no recipes match.

## Technology
- Java
- Android Studio
- SQLite / SQLiteOpenHelper
- RecyclerView
- Android Activities and Intents
- SharedPreferences for the settings preference

## Database
SQLite was selected because the application is designed as a local pantry manager. It provides persistent on-device storage without requiring a separate server or internet connection. The database contains pantry ingredients, recipes and recipe ingredients.

## Project Structure
```text
app/src/main/java/com/example/smartpantry/
├── adapter/
├── database/
├── model/
├── util/
├── AddEditIngredientActivity.java
├── PantryActivity.java
├── RecipeDetailActivity.java
├── SettingsActivity.java
└── SuggestedRecipesActivity.java
```

## Setup and Run
1. Install Android Studio.
2. Open the project folder in Android Studio.
3. Allow Gradle synchronization to complete.
4. Select an Android emulator or connected Android device.
5. Click Run.
6. Open Pantry and add ingredients.
7. Open Suggested Recipes to test strict matching.

## Strict Matching
A recipe is suggested only when every required ingredient:
1. Exists in the pantry.
2. Has at least the required quantity.
3. Has a compatible unit.
4. Can be matched after simple ingredient-name normalisation.

## Demonstration Test
Example:
- Eggs: 2 pieces
- Tomatoes: 2 pieces
- Onion: 1 piece
- Salt: 1 pinch

If one required ingredient is missing, the recipe must not be suggested. After the missing ingredient is added in sufficient quantity, the recipe can appear.

## GitHub
Repository URL:
https://github.com/kwanele4/SmartPantryManager.git

## Student Information
- Student name: Kwanele
- Student number: N/A
- Module: Mobile App Development 700
