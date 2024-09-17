Breakout is an arcade game where a layer of bricks lines the top third of the screen, and the goal is to destroy them all by repeatedly bouncing a ball off a paddle into them. 

Here is a free online version of the game to play so you can get a feel of what the finished product should look like: https://elgoog.im/breakout/

This is based on when Google had an easter egg where the browser automatically pulled up this game when you searched "Atari Breakout" images.

# Module 13: Breakout Game Part 1

First, load up the web page as it is right now, and read the existing code. Familiarize yourself with everything, and ask questions about what is going on before you spend too much time lost. This is a big project, and each student is expected to spend some time talking to the instructor.

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

7. Create a new function that draws a 15x100px rectangle at the bottom center of the canvas.

*Feel free to use ctx.fillStyle to color your paddle and ball differently*

8. add keydown and keyup event listeners to the DOM, and create two new functions for each event. Create two boolean variables called moveLeft and moveRight that are true when their respecitve key is down, and false when it is up.

9. Change the paddles drawn x position to be a variable instead, and in the draw function, check if moveLeft or moveRight is true. This is where you adjust the x position of the paddle to 


# Module 14: Breakout Game Part 2

-modify the ball's code to collide with the paddle

-add the bricks 

-add collision detection to the bricks

-make the bricks disappear when hit


And for the first part of the project, that will probably be it.
