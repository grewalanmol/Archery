## CS174A Team Project - Team 1: Interplanetary Archery

#### Team Members:

- Jeremy Tsujihara, [jtsujihara@ucla.edu](mailto:jtsujihara@ucla.edu), UID: 505311626
- Anmolpreet Kaur, [anmolgrewal@ucla.edu](mailto:anmolgrewal@ucla.edu), UID: 105492836
- Afnan Kamran, afnankamran38@gmail.com, UID:305432648
- Gabriel Goch, gabrielgoch@ucla.edu, UID: 205088483



#### Game Description

This project has users launch projectiles at targets to advance through 3 timed stages. Each stage represents a different environment, with differing gravities, weather conditions, and atmospheres. Players can learn intuitively how these factors affect the path of projectiles.



#### How to play:

1. The 0th stage is target practice. Here users can click the mouse to learn how the projectile flies. Once the user is ready they can hit the 'start' target to begin the game.
2. Here the 1st stage starts and the user will have 30 seconds to hit the target before the time expires.
3. Repeat step 2 for the 2nd and 3rd stage. These stages will have different environmental factors so users will need to adjust how they aim.
4. If the player completes the three stages before the timer runs out, they win. They can refresh the page or press 'q' at any time to restart.


#### Features

- **Collision detection:** The program will implement collision detection to detect when the projectile hits the target.
- **Physics:** Physics is calculated using the center of mass forces on the projectile. For each frame, the position of the object is calculated and input as its translation matrix. Using basic mechanics equations, the initial velocity and sum of acceleration accomplishes this. The force of gravity, wind resistance, and wind change the position of the object while the change in its velocity changes its orientation.
- **Mouse Tracking:** The program allows users to click the mouse to shoot. The location of the cursor will define the initial velocity of the arrow, letting the user aim for the target.


#### Code Overview

The game is wholly contained within the archery.js and index.html files.
- **Game Logic:** The game is broken into 5 levels labled 0 to 4. Level 0 provides instructions to the user and allows them to learn aiming and firing before being put under time pressure. Levels 1, 2, and 3 are timed sections with varying environmental conditions and dynamic target placement. The player is given 30 seconds in each level to strike the target before the time runs out. If the time expires, the game is over and they must start from the beginning. If the player completes all three stages, they win. Each timed level has a unique environment to communicate these differences to the player.
- **Text Display:** The text is formatted in index.html. The logic and contects of the text are within archery.js.
- **Physics:** The game's physics is accomplished by creating an arrow object with a given position and velocity. A planet object defines the gravity, atmosphere, and wind of the environment. For each frame, the arrows position is updated based on the accerelation affecting it and its initial velocity. The velocity is updated for the next frame. The direction is the arrow points is based on its velocity components. The arrow's orientation each frame is recalculated based on how its velocity changes.
- **Collision detection:** 
- **Mouse Tracking:** The users ability to click to aim and fire is handled through mouse tracking. This is done by setting up mouse controls which track the position of the mouse and adds the event of 'mousedown' which is equivelant to click. On this event the position of the mouse is stored into variables which define the arrows initial velocity, and then the arrow is launched.
- **Scene Drawing:** We used the draw function of shapes to draw variuos scenes. We have 3 differnt scenes for 3 differnt levels. We also added some objects to each scence to make it look more real.
