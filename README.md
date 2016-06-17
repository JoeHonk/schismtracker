# Schism Tracker

Schism Tracker is a free and open-source reimplementation of [Impulse
Tracker](https://github.com/schismtracker/schismtracker/wiki/Impulse-Tracker),
a program used to create high quality music without the requirements of
specialized, expensive equipment, and with a unique "finger feel" that is
difficult to replicate in part. The player is based on a highly modified
version of the [Modplug](https://openmpt.org/legacy_software) engine, with a
number of bugfixes and changes to [improve IT
playback](https://github.com/schismtracker/schismtracker/wiki/Player-abuse-tests).

Where Impulse Tracker was limited to i386-based systems running MS-DOS, Schism
Tracker runs on almost any platform that [SDL](http://www.libsdl.org/)
supports, and has been successfully built for Linux, Mac OS X, Windows,
FreeBSD, AmigaOS, BeOS, and even [the
Wii](http://www.wiibrew.org/wiki/Schism_Tracker). Schism will most likely build
on *any* architecture supported by GCC4 (e.g. alpha, m68k, arm, etc.) but it
will probably not be as well-optimized on many systems.

See [the wiki](https://github.com/schismtracker/schismtracker/wiki) for more
information.

## Download

The latest stable builds for Windows and Linux are available from [the releases
page](https://github.com/schismtracker/schismtracker/releases). Hopefully an
OSX build will be soon to follow! Older builds for other platforms can be found
on [the wiki](https://github.com/schismtracker/schismtracker/wiki).

### Building Schism Tracker

To build Schism Tracker, you should set up a build-directory. From the schismtracker directory:

`mkdir -p build && cd build && ../configure && make`

Schism Tracker can be built using the mingw32 cross-compiler on a Linux host. You will also need the SDL MINGW32 development library. If you unpacked it into /usr/i586-mingw32/, you could use the following to cross-compile Schism Tracker for Win32:

`mkdir win32-build`
`cd build`
`env SDL_CONFIG=/usr/i586-mingw32/sdl-config    \`
    `../configure --{host,target}=i586-mingw32  \`
                 `--without-x``
`make`

### Distribution-specific instructions

Getting the prerequisites covered is fairly straightforward in most Linux distributions.

Ubuntu / Debian

`apt-get install build-essential automake autoconf autoconf-archive          \`
                `libx11-dev libxext-dev libxv-dev libxxf86misc-dev           \`
                `libxxf86vm-dev libsdl1.2-dev libasound2-dev mercurial libtool`

Additionally, for cross-compiling win32 binaries:

`apt-get install mingw32 mingw32-binutils mingw32-runtime nsis`

