Inspired by [this comment,](https://github.com/swaywm/sway/issues/4882#issuecomment-611464474) this is a sway config file for adding icons in title bars using [Font Awesome](https://fontawesome.com/search?o=r&m=free).

Normally, this is very tedidous to do; so to not waste time on a grand scale with everyone manually trying to specifiy an icon for each app, I decided to make this repo as a shortcut for people who are interested.

# Usage

1. Install Font Awesome, if not already installed.

Arch-based:
```
sudo pacman -S ttf-font-awesome
```

Debian-based:
```
sudo apt install fonts-font-awesome
```

2. Copy the `icons` file to `~/.config/sway`

3. Add line...
```
include icons
```
...to `~/.config/sway/config`

# Contribution

If there are any apps that I haven't added an icon for yet; please open an issue with the `app_id` or `class` of the application that's missing an icon.

You can find the app_id/class by launching the app and running `swaymsg -t get_tree` in a terminal.
