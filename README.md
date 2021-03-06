About TeXworks
==============

TeXworks is an environment for authoring TeX (LaTeX, ConTeXt, etc) documents,
with a Unicode-based, TeX-aware editor, integrated PDF viewer, and a clean,
simple interface accessible to casual and non-technical users.

TeXworks is inspired by Dick Koch's award-winning TeXShop program for Mac OS X,
which has made quality typesetting through TeX accessible to a wider community
of users, without a technical or intimidating face. The goal of TeXworks is to
deliver a similarly integrated, easy-to-use environment for users on other
platforms, especially GNU/Linux and Windows.


Further Information
===================

If you find any bugs/problems or have any recommendations, don't hesitate to
stop by the development webpage, send a mail to the mailing list (preferably via
the "Help > Email to mailing list" menu item which automatically includes some
debug information), or file a bug report.

- Homepage:     http://www.tug.org/texworks/
- Development:  https://github.com/TeXworks/texworks
- Bugs:         https://github.com/TeXworks/texworks/issues
- Mailing list: http://tug.org/mailman/listinfo/texworks


License
=======

TeXworks is copyright (C) 2007-2016 by Jonathan Kew, Stefan Löffler, and Charlie
Sharpsteen. Distributed under the terms of the GNU General Public License,
version 2 or (at your option) any later version.
See the file COPYING for details.

The SyncTeX code is copyright (c) 2008-2011 by Jérôme Laurens; see
src/synctex_parser.c for license details.


Building TeXworks
=================

Notes by Jonathan Kew, updated 2011-03-20 and 2015-03-29 by Stefan Löffler

To build TeXworks from source, you will need to install developer packages (or
equivalent) for:

 - Qt (4.6.0 or later)
   http://www.qt.io/download/

 - Poppler (using the latest stable release, currently 0.16, is strongly
   recommended, although versions as old as the 0.6 series should still work)
   http://poppler.freedesktop.org/

 - Hunspell (release 1.2.8 or later is recommended; earlier 1.2.x releases may
   be used, although support for some non-Latin-script languages may be lacking)
   http://hunspell.github.io/

along with their dependencies (such as Freetype, fontconfig, zlib, etc.) If you
also want to build the scripting plugins (optional), you additionally need
development packages for Lua and/or Python. Details will depend on your
platform. On Linux or similar systems, your package manager can probably provide
all these.

Once everything is set up, create a folder for building (e.g., "build") and run
CMake in it to create a Makefile or Xcode project. Finally, run make or use
Xcode to build the application.

The current TeXworks prototype has been successfully built with
 - Xcode (using gcc 4) on Mac OS X (built on 10.5, but should run on 10.4 or
   later)
 - MinGW release 5.1.4 on Windows XP (also runs on Vista and Windows 7)
 - gcc 4 on GNU/Linux, various BSDs, etc.

On the Mac, required libraries can be obtained, e.g., using Homebrew.

Further tips on building TeXworks from source are available on some of the wiki
pages:
 - https://github.com/TeXworks/texworks/wiki/Building
 - https://github.com/TeXworks/texworks/wiki/Building-on-Windows-(MinGW)
 - https://github.com/TeXworks/texworks/wiki/Building-on-Mac-OS-X-(Homebrew)
