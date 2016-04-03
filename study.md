# Game Project Scope Study

## Required Readings

-   [Game Project](https://github.com/ga-wdi-boston/game-project)
-   [Game API](https://github.com/ga-wdi-boston/game-project-api)
-   [What is a User Story](http://searchsoftwarequality.techtarget.com/definition/user-story)

## Deliverables

After reading the `game-project` prompt and the `game-project-api` documentation
please do the following and be prepared to share and discuss on Monday morning.

Submit detailed answers to these in this file via a pull request.

-   A wireframe of what your game project will look like.
-   The data structure you plan to use.
  - How you will take the markup of the game board and represent it in JS
-   How you plan to approach this project.
-   4-8 user stories for your game project.
-   How you plan to keep your code moodular.
-   What creative spin will you add to your project.
-   How you will use version control to backup / track your project.
-   Do you plan to attempt any of the bonuses.

-Data Structure:

I admittedly have almost zero experience with this, so my plan was to strictly follow KISS mentality. I think that I could use a simple array (length 8) and assign each square of the board to an index (0-8). I could then create win cases  such as
if (board[0] === “X” &&
    board[1] === “X” &&
    board[2] === “X”) { return playerWins( X ) };

That being said, there will be a lot of win-cases (8 per player) and I will also have to build a turn counter so that if ( turns === 9 && !winner ) {return tie}.

Users IDs will be stored as an object nearly identical to what we did on Thursday/Friday.

-Markup > JS

My plan was to make an HTML table (3 x 3) with individual id's for each respective square (0 - 8). These squares would be assigned a value of X or O when clicked, depending on the player activated. The value of each square will then be updated to the boardArray which will run a loop to determine if there is a winner, or game play should continue (aka activate next player). Using jQuery and CSS (:hover) I can create a simplistic, yet effective UX which will promote engagement as well as clarity (e.g. highlight square when hovered over). I will use responsive design with a single media query (max-width: 800px) to switch between layouts.

-Approach

Given my experience so far, and Antony's repeated warnings, my approach is to build one line at a time. I will begin by creating the HTML table and testing my win-cases/game play by allowing for manual input of X or O. Next, I will add the turns feature which will alternate players. After that, I will add the log-in log-out feature, followed by the win-counter.

Once these are functioning properly, I will add the navBar/options which will allow players to reset a game, log-out, and change color scheme.

I plan to use Sass color formulae so that I can easily create 3-4 color schemes.

Through every step I will be testing on a local rails server and httpbin.org.

-User stories

user story 1: I am about to make a selection on the board, but I want to make sure I am selecting the right square.
Developer: In order to insure transparency and increase user engagement, I will develop a css :hover property to indicate on which square a users' move will fall.

User Story 2: I want to log into this awesome Tic-Tac-Toe app, so that I can play.
Developer: User log-in will be prominently displayed, and mandatory for user to play.

User Story 3: I have been playing this game for a while now, and I can no longer remember how many games I have won.
Developer: A counter for wins (and ties) will be built into the app allowing players to track their progress and track their dominance.

User Story 4: I am having a difficult time seeing the board with the current color scheme.
Developer: Multiple color schemes will be available by utilizing Sass's color alterations functions. This is a (relatively) easy feature that will dramatically improve the user's experience.

-Modularity

I plan to keep my code modular by utilizing callback functions whenever appropriate. This will not only decrease the potential for errors, but also make my code DRY, and allow for easier addittion/alteration as my user base (and sales) increases. It will allow me to add more features more easily, and it will also make debugging easier because I will be able to debug small functions seperately.

-Creative Spin

By adding the option to alter the color scheme, I will be allowing the user to have a (small) level of customization. If I am able to complete my app with time to spare, I would also like to add a series of animations to the selection. This will probably require me to represent the text values of X and O as .svg so that I can fully utilize CSS/Sass's extensive transform capabilities.

That being said, I am more focused on function. UI/UX enhancements and creativity are secondary.

-Version Control

I will utilizing version control extensively throughout this project. My plan is generate a version for backup/milestones every time I summit a challenge. I anticipate many challenges, and therefore many versions.

-Bonuses

I would love to be able to enable network play for a variety of reasons, but I am not even going to consider it until I have the app working with the features I am excited about (color schemes, animations).

Ask me in a few days.
