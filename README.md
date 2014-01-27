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

## BUGS

While this initial draft is an interesting start, there are
so many things to fix....

* No examples or documentation
* This program is *not* cross platform: it only works on GNU/Linux (and is probably very sensitive
  to the windowing manager and desktop configuration)
* Tests.
  Where are the unit tests? (gimme a Jenkins template, please!)
* Mouse drag is wonkly.
  Right now the only "safe" way to record mouse drag events is to drag
  "in the blind" in the yxcba window, then release the mouse, and have the events
  get sent to the target window.  There *must* be a better way.

## Thanks

This technical study would not have been possible without the patient
coaching from [Kieth Packard](http://keithp.com/) and the XCB examples I could find:

* XCB links here...

## Copyright and license

Copyright © 2014 Tom Marble
Licensed under copyleft-next | AGPv3+

This means that this work is disjunctively licensed under the
copyleft-next version 0.3.0 (or later), or at your option,
under the GNU Affero General Public License version 3 (or later).

FFI:
* https://github.com/richardfontana/copyleft-next
* https://www.gnu.org/licenses/agpl-3.0.html
