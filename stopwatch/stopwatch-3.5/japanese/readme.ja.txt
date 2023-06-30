This is readme.ja.txt, edited by Green, originally comes from the author.

I replaced original English strings with Japanese for the convenience of
users in Japanese language environment.

6/26/23 the first version of Japanese translation,
        by Green <usergreen@users.sourceforge.net>


This is the README file for stopwatch, a program that implements a
stopwatch. The author wrote it to help him time talks or individual slides
within a talk. For that purpose, it works well.

--------------------
To Install
--------------------

See the install instructions at https://expect.sourceforge.net/stopwatch/#install

--------------------
To Use
--------------------

See the directions at https://expect.sourceforge.net/stopwatch/#directions

--------------------
Systems Supported
--------------------

Stopwatch should work on any system that supports Tk 8.3 or later.
For earlier versions, see: https://expect.sourceforge.net/stopwatch/

--------------------
Author
--------------------

Don Libes
National Institute of Standards and Technology
Bldg 220, Rm A-127
Gaithersburg, MD  20899
(301) 975-3535
libes@nist.gov


----------------------------------------------------------------------
----------------------------------------------------------------------

The below is the HISTORY file for stopwatch.

Date	Version	Description
-------	-------	------------------------------------------------------
10/26/04 3.5	Made keyboard shortcuts orthogonal and added shortcuts to the
		help.

6/23/04	3.4	At request of Michel Bellemare <michel_bellemare@uqtr.xca>,
		added keyboard bindings for all buttons.

9/6/03	3.3	Made zero button work even when clock is running.  Made 
		shift-zero or shift-record do "record and log" to support
		functionality of a real stopwatch.

6/30/03	3.2	Added support for "Select All".

6/17/03 3.1	Added support to enable/disable milliseconds from menu.

5/6/03	3.0	Added code to countdown and stop at zero.  Added menus to
		support this configuration.  Added help.  Just about doubled
		size of overall script.  Was 211, is 416!

7/11/02 2.6	Bernhard Kuemel <bernhard@rainbow.hn.org> noted stopwatch no
		longer worked in non-msec mode.

5/14/02 2.5	Vertical expansion of widgets wasn't working properly.  Fixed.

1/28/02 2.4.1	Make code more readable.

1/25/02 2.4	Noted that hours overflowed at 596.  Fixed it so that if
		millisecond timing is turned off, the additional bits are given
		back so that additional hours can be tracked.

		Added binding for Return to start/stop the clock.

1/24/02 2.3	Further cleaned up the code and display.

1/23/02 2.2	Mark Saye <markgsaye@yahoo.com> pointed out a bug and suggested
		the whole implementation was unnecessarily complex.  He was
		right.  There's no need to sync the msec and second clocks
		because the msec clock has enough bits.

1/22/02 2.1	Ben Blackhawk <bblackhawk@providenceacademy.org> noted that
		new version broke in the browser.  Added a test for tclversion
		so that it disables millisecond code if running in an older
		version.

1/17/02 2.0	Rich Biolnick <bilonick@stat.cmu.edu> asked for millisecond
		timing and I started fiddling and a couple hours later had
		it done.  It was mildly unpleasant because Tcl doesn't
		provide access to absolute msec time.  There is a msec timer
		but it's relative so you have to establish synchrony between
		the two timers yourself.

		Also worked on display - to make it expand the log when the
		user expands the window.  It's almost right.  But there's
		still a bug in the grid propagation code which I haven't
		tracked down.

6/12/00	1.2	Angel De Vicente <angelv@dai.ed.ac.uk> added a simple log.
		Rewrote log to be more generic (log either time at any time)
		and made it able to do splits like a real stopwatch.  Added
		autoselection.

		Adjusted fonts after realizing that courier really wasn't
		necessary for formatting (and is horribly ugly).

		Added some color highlights.

3/31/98 1.1	Dave Marquardt <marquard@austin.ibm.com> found typo which
		caused mishandling of hours.

4/8/01	1.2	Liebrecht <Lrven@attglobal.net> reported failure in the
		plugin because tk_setPalette tries to create a toplevel.
