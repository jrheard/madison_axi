.. |madison_axi| replace:: :mod:`madison_axi`

Welcome to madison_axi's documentation!
=======================================

Overview
--------

|madison_axi| is a Python library that allows users to directly control an
`AxiDraw <http://axidraw.com>`_ by writing Python code.
Its source code is on `GitHub <https://github.com/jrheard/madison_axi>`_.

If you'd just like to get started, check out the :doc:`quickstart` guide.

The AxiDraw is a really neat little robot that can be controlled in a number of ways.
The standard way of using an AxiDraw is to use a program like RoboPaint or Inkscape,
draw a picture with your mouse/trackpad, and then basically hit a "print" button that sends the picture
to the bot, which then automatically paints it on a piece of paper. For more information, see
`the bot's official documentation <https://wiki.evilmadscientist.com/Axidraw_Software_Installation>`_.

|madison_axi| is a little bit different: rather than having you draw a picture by hand
using a mouse or trackpad, |madison_axi| lets you control the bot directly by writing Python code.
You write a line like ``pen_up()`` and the bot lifts the pen away from the page;
you write ``move_forward(100)`` and the bot moves the pen "forward" 100 "steps"; etc.

The library also makes use of the ``turtle`` module in order to allow users to visualize
what their program will paint when it's connected to the AxiDraw.

|madison_axi| was written for use in an intermediate Python class in Madison High School
in Portland, Oregon.

Useful pages
------------

.. toctree ::
    :maxdepth: 2

    quickstart
    madison_axi
