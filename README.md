# Slaap it!
The classic Pong game recreated using Python

## My Contributions:

- Implemented ball-paddle collision
- Implemented the scoring system and resetting the ball for multiple rounds
- Designed the user interface GUI for the main menu , win/lose screen, and scoring system

## Index

### Game Features:
- The start screen contains Single Player, Two Player and Quit Game buttons:
    - Click on the Single Player button to start playing the single player mode
    - Click on the Two Player button to start playing the two player mode

### Installation and Running:
#### For Windows:
Python3 and pygame module are required to run this game.

To install the pygame module, visit https://www.pygame.org/download.shtml.

Clone the repo and run view.py.

#### For Linux:
Python3 and pygame module are required to run this game.

To install python3, run the following command:
```
sudo apt-get update
sudo apt-get install python3
```

To install pygame module run the following command:
```
sudo apt-get install python-pygame
```

Clone the repo and run view.py.

### Controls:
|Button|Action|
|------|------|
|W key|Player 1 moves up|
|S key|Player 1 moves down|
|Down key|Player 2 moves down|
|Up key|Player 2 moves up|

In Single Player mode, the player uses the Player 1 controls to move the left paddle.
- Instructions:
    - The players need to use their paddle to prevent the ball from colliding with the wall
    - If a player misses the ball, the other player will get one point
    - The first player to earn 5 points wins

### Screenshots:

![Main Menu](https://github.com/anusha246/Slaap-It-Pong-Game/blob/master/Screenshots/Screenshot%20from%202019-03-19%2013-23-58.png)

![Gameplay](https://github.com/anusha246/Slaap-It-Pong-Game/blob/master/Screenshots/Screenshot%20from%202019-03-21%2018-07-04.png)


## Code Structure:

The code is designed using the Model View Controller and Strategy design patterns for code clarity and extendibilty.

- The file view.py contains the main loop which initializes and updates the game screen. It is also the View component of the MVC pattern.

- The file controller.py contains the Controller component of the MVC pattern. It is responsible for sending all the data related to user input, paddle initiation, ball collision, and game modes.

- The files ball.py, user.py and paddle.py are the Model component of the MVC pattern and are responsible for initializing the ball, the user(s) and the paddle(s) for the game. Furthermore, user.py is a parent class for person_player.py and computer_player.py and is designed around the Strategy design pattern.

- The game is designed so that additional features are straightforward to add. 

For example: 

To add a new button "button_x" to the main menu, simply open view.py and add the following code to Line 21:
```
menu_options = ["Single  Player", "  Two Player", "  Quit Game", "x_button"]
button_x = pygame.draw.rect(window, (2,5,100), (150, 310, 200, 50))
```

### Contributors (SLAAP Team):
- Sidharth Khurana

- Lingxiao Liu

- Anusha Pahore

- Ashir Riaz

- Pushti Gandhi


### License:

Built under GNU General Public License

You can find a copy of the License in the LICENSE.
