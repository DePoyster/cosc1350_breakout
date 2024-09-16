# Breakout Game TODO

First, load up the web page as it is right now, and read the existing code. 
Familiarize yourself with everything, and ask questions about what is going on 
before you spend too much time lost. This is a big project, and it is expected
that each student spends some time talking to the instructor.

## Make the web page look more appealing

Before getting to far into the hard stuff, it would be nice if what you're
working on is not a complete eyesore. 

1. Label the breakout game with a header. 
*Perhaps something like an h1 tag with the content 'Breakout Game'.*

2. Center the header and canvas elements on the page. 

3. Style the rest of the page to your liking.
*At a minimum, add a colored background and a border around the breakout game. A cool font would be nice*

## Get the ball moving

4. Uncomment the lines of code in the draw function to make the ball's position change.

5. Check if the ball hits the width of the canvas element. If so, negate the xMoveDist.
*hint: if(xPos >= canvas.width) xMoveDist = -xMoveDist;*

6. Do the same for the height of the canvas element and the yMoveDist.

7. Draw a 15x100px rectangle at the bottom center of the canvas element to act as the paddle.
*This will move side to side and be what the player uses to *
<img src=./graygeto.jpg>