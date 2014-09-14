# <s>m</s>werlin</h1>

*<s>m</s>werlin* is a presentation tool for HTML-based slideshows. This is a
quick hack I have written for my [JS:Inception
talk](http://perezdecastro.org/jsinception) talk at [JSConf EU
2014](http://2014.jsconf.eu). It uses WebKitGTK2 and VTE stacked in the same
window to provide quick keyboard-based switching between the slides and
a terminal (which can be used for live coding demos, for example). On top of
that, all opened windows will all show either the terminal or the slides,
and they status of the view will be synchronized among windows: the slides
and presenter notes will be different in both windows, but their terminals
can be made to show the same content (by now, using ``tmux``), so when
making live demos both the presenter and the audience will see the same.

[ ![](https://raw.githubusercontent.com/aperezdc/mwerlin/master/images/mwerlin-small.gif) ](https://raw.githubusercontent.com/aperezdc/mwerlin/master/images/mwerlin.gif)

## Requirements

* [Lua](http://lua.org) 5.2.
* [LGi](https://github.com/pavouk/lgi/).
* [GTK+](http://www.gtk.org), version 3.10 or newer.
* [VTE](https://developer.gnome.org/vte/unstable/), version 2.77 or newer.
* [WebKitGTK2](http://webkitgtk.org), version 2.4.4 or newer.

If you are on [Arch Linux](http://archlinux.org) you can get the
dependencies installed with a single command:

    pacman -S webkitgtk2 lua-lgi vte3


## Usage

1. Run ``mwerlin``.
2. Press the “Open” button in the header bar, and choose the HTML containing
   file containing your slides.
3. Attach to the same ``tmux`` session in the terminals of both windows.
4. Open the presenter view. For
   [impress.js](https://github.com/bartaz/impress.js) this can be done
   pressing ``P`` in the keyboard. A new window will pop-up.
5. Move the presentation window to the projector or screen used to show the
   slides, and make it fullscreen pressing ``Ctrl-F``.
6. Move the speaker notes window to your screen, make it fullscreen as well,
   again using ``Ctrl-F``.
7. Go over your presentation. Whenever you want to switch between slides
   view and the terminal, press ``Ctrl-1`` and ``Ctrl-2``.


### Key bindings

* ``Ctrl-1``: Switch to presentation view.
* ``Ctrl-2``: Switch to embedded terminal.
* ``Ctrl-F``: Make a window fullscreen.
* ``Ctrl-U``: “Un-fullscreen” a window.

