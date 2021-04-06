# 4.3BSD Quasijarus

### Why?

I already did [Research Unix Verion 7](https://github.com/narukeh/research_unix_v7), so why not this too?

----

This is the result of following the [tavi.co.uk/unixhistory/quasijarus.html](https://www.tavi.co.uk/unixhistory/quasijarus.html) page.

Everything is ready. I did it so you dont have to. I have installed 4.3BSD Quasijarus and **NOTHIG** else. So you have a pure system.

From here you can do what you want. I would suggest to copy/backup the file `quasdisk.dsk`, if you mess things up, you can easily revert.

----

What else you need: Nothing really (if you're using a 64bit linux distro), i even included the vax emulator. But you should be using your Distros `simh` package, which should be having the latest version.

----

### Contents:

- File `vax`: Its from [official simh](https://github.com/simh/simh/releases/tag/v3.8-1) repo, version 3.8.-1. Use this if your distro doesnt have the `simh` package, or if it wont work with this project. This is a x86_64 binary. [SimH Github Repo.](https://github.com/simh/simh/)
- File `quasdisk.dsk` is the "disk" of the system. Thats where the system is installed. make a copy of it for backup.
- Files `boot.ini  init.ini  vax_better.ini  vax.ini` are configs for the SimH emulator.
- Directory `src`: Every file mentioned in [tavi.co.uk/unixhistory/quasijarus.html](https://www.tavi.co.uk/unixhistory/quasijarus.html) page. So you have everything you need if you want to do it yourself.
- Directory `docs/`:
	- File `quasijarus.html`: The main documentation. If you want to do it yourself, this is all you need.
	- File `Installing_4.3_BSD_Quasijarus_on_SIMH.html` is in readable form of `gunkies.org/Installing 4.3 BSD Quasijarus on SIMH - Computer History Wiki.html`, which is a recommended read.

----

### How to:

FIRST: Uncompress the disk image `quasdisk.dsk.xz`. I had to compress the disk image. Github limit it 100Mb.

`unxz quasdisk.dsk.xz`

Read the [quasijarus.html](docs/quasijarus.html#stage4) stage 4. But Here is a **very short** tutorial, to **just** start it:

>type `./vax vax.ini` and it will start
>
>wait to prompt, then type `b`
>
>wait for login prompt, then type `root`
>
>if root has a password, its `password`.
