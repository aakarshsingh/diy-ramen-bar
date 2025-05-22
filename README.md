
# DIY Korean Ramen Bar 🍜

_Craft your ultimate ramen bowl, discover its funkiness, and share your masterpiece!_

Welcome to the DIY Korean Ramen Bar! This is a fun, interactive web application that lets users create their own custom Korean ramen bowls, discover a "funkiness level" based on their choices, and even export a shareable image of their creation.

## Features

-   **Interactive Ingredient Selection:** Users can choose from a variety of ramen bases, proteins, vegetables, crunchy toppings, and condiments.
    
-   **Dynamic Ramen Naming:** Get a unique, fun name for your ramen creation based on your selections.
    
-   **Funkiness Meter:** A "funkiness" score is calculated based on the chosen ingredients, with special ingredients adding more weight. A random factor keeps it surprising!
    
-   **Leaderboard:** Save your ramen creation with your name to a local leaderboard and see how your funkiness compares to others.
    
-   **Export as Image:** Generate a visually appealing "recipe card" image of your ramen creation, perfect for sharing on social media. Uses `html2canvas.js`.
    
-   **Admin Panel:**
    
    -   Clear the leaderboard.
        
    -   Export leaderboard data as JSON.
        
    -   Manage ingredients:
        
        -   Add new ingredients to any category.
            
        -   Mark ingredients as "special" to influence the funkiness score.
            
        -   Remove ingredients.
            
        -   Reset all ingredients to their default settings.
            
-   **Persistent Storage:** Uses `localStorage` to save custom ingredients and leaderboard entries.
    
-   **Responsive Design:** Adapts to different screen sizes for a good user experience on desktop and mobile.
    

## How It Works

The application is built with HTML, CSS, and vanilla JavaScript.

-   **HTML (`index.html`):** Structures the main page, including sections for ingredient selection, the ramen display, leaderboard, admin panel, and modals.
    
-   **CSS (inline `<style>`):** Handles all the styling for the application, including layout, colors, fonts, and responsiveness. It also includes specific styles for the recipe card image export.
    
-   **JavaScript (inline `<script>`):**
    
    -   Manages the application's state (current selection, ingredients, leaderboard).
        
    -   Dynamically loads ingredient options onto the page.
        
    -   Calculates the "funkiness" score and generates ramen names.
        
    -   Handles user interactions (selecting ingredients, saving to leaderboard, admin actions).
        
    -   Uses `html2canvas.js` (included via CDN) to convert the recipe card HTML into a downloadable PNG image.
        
    -   Uses `localStorage` to persist custom ingredients and leaderboard data across sessions.
        

## Setup

1.  Simply open the `index.html` file (or the main HTML file you've named it) in a modern web browser.
    
2.  No server-side setup is required as it's a client-side application.
    

## Key JavaScript Functions

-   `loadCustomIngredientsToPage()`: Populates the ingredient selection areas.
    
-   `updateSelection()`: Called whenever an ingredient or guest name changes, recalculates everything.
    
-   `calculateFunkiness()`: The core logic for determining the funkiness score, now with special ingredient weighting and a random factor.
    
-   `generateRamenName()`: Creates a fun name for the ramen.
    
-   `updateDisplay()`: Refreshes the UI elements like ramen name, funkiness meter, and selected ingredients list.
    
-   `saveToLeaderboard()`: Adds the current creation to the leaderboard.
    
-   `exportRecipeAsImage()`: Uses `html2canvas` to generate and download the recipe card image.
    
-   **Admin Functions:**
    
    -   `openIngredientManager()`, `closeIngredientManager()`
        
    -   `populateIngredientsInModal()`, `addIngredientFromModal()`, `removeIngredientFromManager()`, `toggleIngredientSpecialStatus()`
        
    -   `resetIngredientsToDefaults()`
        
    -   `clearLeaderboard()`, `exportLeaderboardData()`
        

## Customization

-   **Ingredients:** Modify the `defaultIngredients` object in the JavaScript to change the initial set of available items, their categories, and their "special" status.
    
-   **Ramen Names & Fusion Combos:** Edit the `ramenNames` and `fusionCombos` arrays in the JavaScript to add more variety.
    
-   **Styling:** All CSS is within the `<style>` tags in the HTML file and can be modified to change the look and feel.
    
-   **Funkiness Algorithm:** The `calculateFunkiness()` function can be tweaked to adjust how scores are awarded.
    

## Future Enhancements (Ideas)

-   More sophisticated visual cues for special ingredients.
    
-   Ability to upload custom images for ingredients.
    
-   User accounts and a server-side leaderboard for global competition.
    
-   More detailed recipe instructions based on selections.
    
-   Theming options for the UI.
    

Enjoy creating your ultimate funky ramen! 🍜✨
