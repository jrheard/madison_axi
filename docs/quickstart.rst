QuickStart
==========

Installation
------------

To install the library, run ``pip install madison_axi`` at the command line. Now you're ready to draw some pictures!

How to draw stuff on your computer screen
-----------------------------------------

Here's a short Python program that draws a box in the middle of your computer screen (and on your AxiDraw, if it's plugged into your computer)::

    # Import all the functions in the `madison_axi.axi` module.
    from madison_axi.axi import *

    # IMPORTANT: You MUST call initialize() at the
    # start of your program. It won't work otherwise.
    initialize()

    # Get ready to draw a box: move to the top-left
    # corner of the box we're going to draw.
    move_to(-50, 50)

    # Point in the direction of 0 degrees, which is
    # straight to the right.
    point_in_direction(0)

    # Put the pen down.
    # If we didn't include this line, nothing would get drawn!
    pen_down()

    # Do this next bit four times:
    for i in range(4):

        # Move forward a hundred steps, then
        # turn ninety degrees to the right.
        move_forward(100)
        turn_right(90)

    # We've finished drawing our box!
    # Always call cleanup() at the end of your program.
    cleanup()

    # Wait for the user to press Enter before exiting the program.
    # Without this line, the program would draw a box
    # on the screen really fast, then close the turtle window
    # _immediately_ before the user had a chance
    # to look at the picture their code drew!
    input("Done! Press Enter to close the program.")

The important things to remember are that you **must** call ``initialize()`` at
the beginning of your program, and that you should also call ``cleanup()`` at
the end of your program. Aside from that, go nuts!

Note: When you run your program, you'll see a small window on your screen that
simulates what'll happen when you have the AxiDraw draw your picture.
**Make sure that your picture stays within the bounds of that small window**;
anything that you draw outside of that window will not get drawn when you
run your program on the actual bot.

To see a list of all of the different functions you can use to control the bot,
click on this link: :mod:`madison_axi`. You can also read the library's
`source code <https://github.com/jrheard/madison_axi/blob/master/madison_axi/axi.py>`_,
it really isn't very long.

How to actually draw pictures on the AxiDraw
---------------------------------------------------

``madison_axi`` uses a program called CNC Server to control the AxiDraw.
In order to have your Python program draw pictures on the bot, go to the
`CNC Server README <https://github.com/techninja/cncserver/blob/master/README.md>`_ and follow
the instructions in the **Installation** and **Running** sections. When you run CNC Server,
be sure to specify that you've got an AxiDraw plugged in.

Once you've done that, you're good to go - when you run a program that uses :mod:`madison_axi`,
it should automatically draw stuff on the robot as well as on your screen.

More Example Programs
---------------------

``madison_axi`` comes with a few `example programs <https://github.com/jrheard/madison_axi/tree/master/madison_axi/examples>`_
that you can use as starting points. Read through them, try to predict what they'll do or just copy-paste them
into your editor and run them yourself! My favorite one's spiky_circle, check it out. Once you've got
one of them running, try making a change to it and see what happens,
and then make more changes, and just generally keep going and have a great time. Play around!
