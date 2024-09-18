Breakout is an arcade game where a layer of bricks lines the top third of the screen, and the goal is to destroy them all by repeatedly bouncing a ball off a paddle into them. 

Here is a free online version of the game to play so you can get a feel of what the finished product should look like: https://elgoog.im/breakout/

This is based on when Google had an easter egg where the browser automatically pulled up this game when you searched "Atari Breakout" images.

# Module 13: Breakout Game Part 1

First, load up the web page as it is right now, and read the existing code. Familiarize yourself with everything, and ask questions about what is going on before you spend too much time lost. This is a big project, and each student is expected to spend some time talking to the instructor. These instructions are not enough to successfully code this game; it will take creativity, intuition, research, and above all, questions.

## Make the web page look more appealing

Before getting too far into the hard stuff, it would be nice if what you're working on is not a complete eyesore. 

1. Label the breakout game with a header. 

*Perhaps something like an h1 tag with the content 'Breakout Game'.*

2. Center the header and canvas elements on the page. 

3. Style the rest of the page to your liking.

*At a minimum, add a colored background and a border around the breakout game. A cool font would be nice*

## Get the ball moving

4. Uncomment the lines of code in the draw function to make the ball's position change.

5. Bounce the ball off the wall by comparing xPos and the boundries of the game, and negating xMoveDist.

*hint: if(xPos > canvas.width - ballRadius) xMoveDist = -xMoveDist;*

6. Do the same for the height of the canvas element and the yMoveDist.

*After this step, the ball should be infinitely bouncing off the walls*

## Add the paddle

7. Create a new function that draws a 100x15px rectangle at the bottom center of the canvas.

*Feel free to use ctx.fillStyle to color your paddle and ball differently*

8. add keydown and keyup event listeners to the DOM, and create two new functions for each event. Create two boolean variables called moveLeft and moveRight that are true when their respecitve key is down, and false when it is up.

9. Change the paddles drawn x position to be a variable instead named xPaddle, and in the draw function check if moveLeft or moveRight is true, and adjust the xPaddle by 3 in the appropriate direction.

*You should now have a paddle that can move left and right! Make sure you don't allow for the paddle to move off the screen as well.*

Before submitting the assignment, double check that you have updated the name and date at the top of the source code files, and have replaced my comments with comments that are meaningful to you. 

# Module 14: Breakout Game Part 2

Now, it is time to line the top of the game with bricks. It is easiest to manage the bricks by defining them as objects with an x position, y position, and hit status. Then, you can use an array to hold your brick objects, and iterate through that array to draw them on the canvas element. After doing that, we will be ready to add collision detection to the game. 

## Define the bricks

1. Define values for the bricks. For this version of breakout, we will have 4 rows and 6 columns of 90x25px bricks. Allow for a 40px space from the top of the game and the top of the brick row. 

* To nicely align the bricks, they should be padded 5px away from the walls, and 10px away from each other. Therefore, your values should be brickRows=6, brickColumns=4, brickWidth=75, brickHeight=20, brickPadding=10, brickTopOffset=40, brickLeftOffset=5. 

2. Define the array of brick objects.

*This is easiest done with two for loops: one to iterate through the rows, and another nested loop to iterate through the columns. Then, you can use which row or column your brick is at to calculate the xy position of the brick.  *

3. Draw the bricks on the canvas element.

*Simply create a function that iterates through your array of bricks, and draws them as rectangles with their corresponding values that should already be defined. Remember to add this function to the draw function.*

4. To add collision detection to the bricks, you will need to compare the ball's position with the position of each brick.

*Again, use a for loop to iterate through the bricks. If the brick hasn't been hit, check if the ball's x position is greater than the brick's x position AND less than the brick's x position plus the brick's width, AND the same for the ball and brick's y positions, then update the brick's hit status. Also, negate the ball's yMoveDist just like if it hit the ceiling of the game.*

5. Go back and edit the brick drawing function to check whether the hit status of the brick indicates to draw the brick or not.

*Notice that the ball only bounces off of the brick if it hasn't been hit yet. Once the brick is hit, it should be invisible and not cause the ball to bounce off of it anymore. The bricks should now be falling victim to the entropy of the ball*

6. Add collision detection to the paddle by modifying the bottom wall of the game's logic in the draw function. 

*Instead of checking if the ball is at the height of the canvas, check if it is at the height of the canvas minus the height of the paddle, and if it's x coordinates are within the paddle's x coordinates, much like how you did it for the bricks. If the ball does not hit the x coordinates of the paddle, then use clearInterval to stop the calling of the draw function. Add an alert or some text to the DOM to let the user know that it is game over*

# Module 15: Breakout Game Part 3

-Surprise! Use this week to get caught up with what you havn't got done yet. 
-add javascript to keep score
-add reset button to the DOM that calls a function that resets the game

