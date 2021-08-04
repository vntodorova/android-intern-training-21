# Create a Tic-Tac-Toe game

You will create an implementation of the [Tic-Tac-Toe](https://en.wikipedia.org/wiki/Tic-tac-toe) game. The app will have the following screens:

## Entry screen
It holds a "New game" button which opens the Game screen, а "Statistics" button which opens the "Statistics" screen and a Settings button, which opens the "Settings" screen.

## Game screen
It's the place where the user plays the game. It shows the game board. Depending on the mode in which the user is playing (1 Player/2 Players) the game starts differently:
- 1 Player - When the user enters the game he/she is assigned with 'O' and the computer is assigned with 'X'. The user plays first in the first round. Then the game starts playing vs dummy "AI", which randomly marks squares on the game board with its respective sign. When the game ends an "You win!" or "You lose!" message is shown for a few second and then a new game starts automatically. 
- 2 Players - When the game starts, it is randomly decided whether 'X' or 'O' will begin the game. There should be a message somewhere on the screen that says "Turn: X-Player" or "Turn: O-Player". When the game ends, a "Player X wins" or "Player O wins" message is shown for a few seconds and then a new game starts automatically.

Whoever won the game, plays first in the next round.

Depending on the game result a "wins" or a "loses" score is incremented. For this you will need to read about [shared preferences](https://developer.android.com/training/data-storage/shared-preferences.html) where you can read/write simple key-value pairs of information. 
For the game board you will need a [custom view](https://developer.android.com/guide/topics/ui/custom-components.html). Read all the sub-articles there, they will be helpful. You'll need to handle touch events in your view so the [Making the View Interactive](https://developer.android.com/training/custom-views/making-interactive.html) part of the tutorial will be helpful. 

**[You gotta keep them separated](https://www.youtube.com/watch?v=1jOk8dk-qaU)** - the custom view should only contain view-related code about drawing, measuring and intercepting touch events. Then you may have a (view-)model of the game board where the current state of the board and the players is kept. You can have classes that contain the game rules and a master game engine class which puts everything together. Different ways to separate rules/UI/mechanics are possible, just don't put everything in the activity/custom view :).

## Statistics screen
Shows 2 tables for each play mode with the number of wins/loses/draws for the 'X' and 'O' player, read from the Shared Preferences.

## Settings screen
From here, the user can switch the play mode and reset the game statistics.

## Add launcher icon
To make the application more user-friendly, add a launcher icon, which is how the app is displayed in the app list. You can read about how to do it [here](https://developer.android.com/studio/write/image-asset-studio). If you need a suitable icon, you can search in [IconFinder](https://www.iconfinder.com/search?q=tic%20tac%20toe&price=free).
