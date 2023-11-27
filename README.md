![image](https://github.com/iguanajuice/sway-font-awesome/assets/125163000/5be1e6b9-6282-4222-ae7f-cbda96e8f152)

Inspired by [this comment,](https://github.com/swaywm/sway/issues/4882#issuecomment-611464474) this is a sway config file for adding icons in title bars using [Font Awesome](https://fontawesome.com/search?o=r&m=free).

Normally, this is very tedidous to do; so to not waste time on a grand scale with everyone manually trying to specifiy an icon for each app, I decided to make this repo as a shortcut for people who are interested.

# Usage

1. Install Nerd Font Symbols, if not already installed.

Arch-based:
```
sudo pacman -S ttf-nerd-fonts-symbols
```
It's also recommended to remove Font Awesome to avoid conflicts:
```
sudo pacman -R ttf-font-awesome
```

2. Copy the `icons` file to `~/.config/sway/`

3. Add line...
```
include icons
```
...to `~/.config/sway/config`

4. Enable pango in sway's config:
```
pango:MyFont
```

# Contribution

If there are any apps that I haven't added an icon for yet; please open an issue with the `app_id` or `class` of the application that's missing an icon.

You can find the app_id/class by launching the app and running `swaymsg -t get_tree` in a terminal.

Things to know before contributing:
* Be sure to update via `git pull` before opening any issues.
* Everything should be sorted alphabetically.
* `app_id` and `class` entries should stay seperated.
* Icon should be wrapped in \<big> and \</big> tags.
* Inbetween \</big> and %title there should be 2 spaces.
* Due to a bug in god knows where, the first \<big> tag must be proceded by a soft-hyphen. You can type this special character by pressing Ctrl+Shift+u, typing "ad", and pressing enter.
