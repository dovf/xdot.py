About _xdot.py_
=================

_xdot.py_ is an interactive viewer for graphs written in [Graphviz](http://www.graphviz.org/)'s [dot language](http://www.graphviz.org/doc/info/lang.html).

It uses internally the graphviz's [xdot output format](http://www.graphviz.org/doc/info/output.html#d:xdot) as an intermediate format, and [PyGTK](http://www.pygtk.org/) and [Cairo](http://cairographics.org/) for rendering.

_xdot.py_ can be used either as a standalone application from command line, or as a library embedded in your python application.

Status
======

_xdot.py_ script became much more popular than I ever anticipated, and there are several interested in improving it further. However, for several years now, _xdot.py_ already meets my own needs, and unfortunately I don't have much time for maintain it myself.

So I'm looking into transition _xdot.py_ maitenance to others: either hand over the maintenance _xdot.py_ to a community or indicate an official fork of _xdot.py_.

I encourage people interested in development of _xdot.py_ to fork the [GitHub repository](https://github.com/jrfonseca/xdot.py), and join the new [mailing list](https://groups.google.com/d/forum/xdot-py).

Features
========

 * Since it doesn't use bitmaps it is fast and has a small memory footprint.
 * Arbitrary zoom.
 * Keyboard/mouse navigation.
 * Supports events on the nodes with URLs.
 * Animated jumping between nodes.
 * Highlights node/edge under mouse.

Changelog
=========

 * **2013-05-12**: Text based node search (by Salva and ludw1g.m3i3r, issue 68)

 * **2012-11-24**: Printing support (by ludw1g.m3i3r, issue 74)

 * **2011-09-01**: Fix forward slash escaping (issue 61)

 * **2011-02-13**: Show dotted lines in xdot (by djs52uk, issue 50)

 * **2010-12-12**: Support images (thanks to Alberto Rodríguez)

 * **2010-01-32**: Add Quit key binding (from sk, issue #30)

 * **2009-09-30**: Add a reload button (fixes issue #22)

 * **2009-09-30**: Properly handle motion-notify-event (from lodatom, issue #24)

 * **2009-09-20**: Automatically reloads open file when it changes (from Robert Meerman, issue #21)

 * **2009-09-20**: Add support for [ColorBrewer Color Schemes](http://colorbrewer.org/) (from to michael.hliao, issue #23).

 * **2009-08-09**: Upload to [PyPi](http://pypi.python.org/pypi/xdot) (thanks to Marius Gedminas, issue #19)

 * **2009-05-24**: Reloads the file on the 'r' key (from peterbjorgensen).

 * **2009-04-09**: Render subgraphs correctly.

 * **2009-03-04**: Support filled bezier shapes.

 * **2009-01-29**: Check for unicode input; check subprocess returncode (from Jaap Karssenberg).

 * **2008-10-27**: Replace pydot and pyparsing by a much faster hand written lexer and parser (issue #9).

 * **2008-09-02**: Make mouse wheel zoom around the mouse cursor rather than center of window (from Marius Gedminas).

 * **2008-09-02**: Handle polylines. Handle ports in node names.

 * **2008-07-27**: Allow to specify the graphviz filter to use.

 * **2008-07-13**: Commit several enhancements done by [Marius Gedminas](http://mg.pov.lt/blog/europython2008-sprints-day-2.html), such as, animated jumping between nodes, highlighted node/edge under mouse, and support to more xdot language features.

Known Issues
============

 * Not all xdot attributes are supported or correctly rendered yet. It works well for my applications but YMMV.

 * Text doesn't scale properly to large sizes if font hinting is enabled. I haven't find a reliable way to disable font hinting during rendering yet.

See also:

  * [github issue tracker](https://github.com/jrfonseca/xdot.py/issues)

  * [googlecode issue tracker](https://code.google.com/p/jrfonseca/issues/list?q=xdot).

Screenshots
===========

[![Profile 1 Screenshot](https://raw.github.com/wiki/jrfonseca/xdot.py/xdot-profile1_small.png)](https://raw.github.com/wiki/jrfonseca/xdot.py/xdot-profile1.png)
[![Profile 2 Screenshot](https://raw.github.com/wiki/jrfonseca/xdot.py/xdot-profile2_small.png)](https://raw.github.com/wiki/jrfonseca/xdot.py/xdot-profile2.png)
[![Control Flow Graph](https://raw.github.com/wiki/jrfonseca/xdot.py/xdot-cfg_small.png)](https://raw.github.com/wiki/jrfonseca/xdot.py/xdot-cfg.png)

Requirements
============

 * [Python](http://www.python.org/download/) (2.6 or 2.7)

 * [PyGTK](http://www.pygtk.org/downloads.html) (2.10 or greater)

 * [Graphviz](http://www.graphviz.org/Download.php)

Windows users
-------------

Download and install:

 * [Python for Windows](http://www.python.org/download/)

 * [GTK+ Runtime for Windows](http://www.gtk.org/download/win32.php)

 * [PyCairo, PyGobject, and PyGTK for Windows](http://www.pygtk.org/downloads.html)

 * [Graphviz for Windows](http://www.graphviz.org/Download_windows.php)

Debian/Ubuntu users
-------------------

Run:

    apt-get install python-gtk2 graphviz

Usage
=====

Command Line
------------

    Usage: 
    	xdot.py [file]
    
    Options:
      -h, --help            show this help message and exit
      -f FILTER, --filter=FILTER
                            graphviz filter: dot, neato, twopi, circo, or fdp
                            [default: dot]
      -n, --no-filter       assume input is already filtered into xdot format (use
                            e.g. dot -Txdot)
    
    Shortcuts:
      Up, Down, Left, Right     scroll
      PageUp, +, =              zoom in
      PageDown, -               zoom out
      R                         reload dot file
      F                         find
      Q                         quit
      P                         print
      Escape                    halt animation
      Ctrl-drag                 zoom in/out
      Shift-drag                zooms an area

If no input file is given then it will read the dot graph from the standard input.

Embedding
---------

See included `example.py` script for an example of how to embedded _xdot.py_ into another application.

[![Screenshot](https://raw.github.com/wiki/jrfonseca/xdot.py/xdot-sample_small.png)](https://raw.github.com/wiki/jrfonseca/xdot.py/xdot-sample.png)

Download
========

  * https://pypi.python.org/pypi/xdot

  * https://github.com/jrfonseca/xdot.py

Links
=====

 * [Graphviz homepage](http://www.graphviz.org/)

 * [ZGRViewer](http://zvtm.sourceforge.net/zgrviewer.html) -- another superb graphviz/dot viewer

 * [dot2tex](http://code.google.com/p/dot2tex/) -- python script to convert xdot output from Graphviz to a series of PSTricks or PGF/TikZ commands.

 * The [pypy project](http://codespeak.net/pypy/) also includes an [interactive dot viewer based on graphviz's plain format and the pygame library](http://morepypy.blogspot.com/2008/01/visualizing-python-tokenizer.html).