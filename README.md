# yxcba

Your XCB Automator

This program is intended to capture and replay GUI interactions.
Most likely you will want to use this to create automated, silent,
headless rich UI unit tests that can be run by Jenkins.

## running

```
$ yxcba -v
```
Instructions TBD...

## invoking yxcba

```
$ ./yxcba -h
usage: yxcba [-h] [-V] [-v] [-i ID] [-n NAME] [-b BORDER_WIDTH] [-r RESOLUTION] [-s SPEEDUP] [-l] [-w WM]
             [-y WM_HEIGHT] [-x WM_WIDTH] [-o OUT] [-e ERR] [-t TEST_INPUT]

optional arguments:
  -h, --help            show this help message and exit
  -V, --version         show program's version number and exit
  -v, --verbose         verbose mode
  -i ID, --id ID        window ID to automate
  -n NAME, --name NAME  window name to automate
  -b BORDER_WIDTH, --border-width BORDER_WIDTH
                        width of yxcba border highlight
  -r RESOLUTION, --resolution RESOLUTION
                        event resolution (ms)
  -s SPEEDUP, --speedup SPEEDUP
                        speed up sleep statements (1.0)
  -l, --list-windows    simply display a list of windows
  -w WM, --wm WM        window manager name (to handle quirks)
  -y WM_HEIGHT, --wm-height WM_HEIGHT
                        window manager height to subtract from the root window size
  -x WM_WIDTH, --wm-width WM_WIDTH
                        window manager width to subtract from the root window size
  -o OUT, --out OUT     output file (stdout)
  -e ERR, --err ERR     error file (stderr)
  -t TEST_INPUT, --test-input TEST_INPUT
                        test input file
$
```

## BUGS

While this initial draft is an interesting start, there are
so many things to fix....

* No examples or documentation
* Must list dependent packages
* Must run code through PEP8 and pylint checkers
* Only works on Python 2.7 (not Python 3)
* This program is *not* cross platform: it only works on GNU/Linux (and is probably very sensitive
  to the windowing manager and desktop configuration)
* Tests.
  Where are the unit tests? (gimme a Jenkins template, please!)
* Mouse drag is wonky.
  Right now the only "safe" way to record mouse drag events is to drag
  "in the blind" in the yxcba window, then release the mouse, and have the events
  get sent to the target window.  There *must* be a better way.

## Thanks

This technical study would not have been possible without the patient
coaching from [Keith Packard](http://keithp.com/) and the XCB examples I could find:

* http://xcb.freedesktop.org/tutorial/
* http://xcb.freedesktop.org/XcbPythonBinding/
* http://xcb.freedesktop.org/manual/
* http://tronche.com/gui/x/

## Copyright and license

Copyright © 2014 Tom Marble

Licensed under { copyleft-next | AGPv3+ }

This means that this work is disjunctively licensed under the
copyleft-next version 0.3.0 (or later), or at your option,
under the GNU Affero General Public License version 3 (or later).

FFI:
* https://github.com/richardfontana/copyleft-next
* https://www.gnu.org/licenses/agpl-3.0.html
