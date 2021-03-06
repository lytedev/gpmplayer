# `gpmplayer` - Google Play Music Player

A simple curses client for Google Play Music.

![Queue mode screenshot][ss1]

I started this project because [thunner][thunner] didn't support Two-Factor
Authentication... or at least I couldn't figure it out. Anyways, writing your
own tool is half the fun, right?

## Disclaimer

This project isn't really all that great to use. So far, it has the absolutely
minimum amount of functionality/usability that I needed and I've basically
stopped there. Please don't expect a full-featured client at this point!

## Dependencies

`gpmplayer` depends on the wonderful [gmusicapi][gmusicapi]. It also uses
appdirs for figuring out where to put its files.

It also uses `mplayer` to actually, y'know, *play* the songs. So you'll need
that installed (and obviously in your PATH) as well.

```bash
sudo pip2 install gmusicapi appdirs
```

## Config

You just need a `config.ini` in `$XDG_CONFIG_HOME/gpmplayer/` in the following format:

```ini
[gpmplayer]
email = your_google_email@example.com
password = app_specific_password
mobile-id = your_device_id
```

You can read elsewhere on how to get the device ID. Apparently you can use your
MAC address or something as well or something, but whatever. You're a smart
person and you'll figure it out.

Once your config is ready, you can fire up the app.

## Usage

Here are the controls:

    j     - Move down
    k     - Move up
    Enter - Select
    p     - Jump to your list of playlists
    z     - Toggle shuffle

Fairly self-explanatory, I think.

## Install

    sudo ln -s "$PWD/gpmplayer" /usr/bin/gpmplayer

## Uninstall

    sudo rm -f /usr/bin/gpmplayer

## Bugs

* None at this moment...? Lots of missing functionality...

## To Do

* Jump to queue view
* Shortcuts (and functionality) for next song, pause, prev song, etc.
* In-playlist/in-queue fuzzy search
* Some way to pipe status out (for displaying on bar)
* Google Play Search/radio functionality
* Moar configuration options
* Better queue management
* Show song progress
* Skipping around in songs
* Non-sucky, configurable interface
* Async goodness
* Parallelize where possible
* Prefetching next few songs
* Caching requests that generally return a larger payload

## License

You can find it [here][license].


[ss1]: https://github.com/lytedev/gpmplayer/blob/pr-assets/screenshots/1.png?raw=true
[thunner]: https://github.com/malcolmstill/thunner
[gmusicapi]: https://github.com/simon-weber/gmusicapi
[license]: https://github.com/lytedev/gpmplayer/blob/master/LICENSE

