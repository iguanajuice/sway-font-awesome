![image](https://github.com/iguanajuice/sway-font-awesome/assets/125163000/7d0f9d47-27e3-4525-8177-c66a70370410)

Inspired by [this comment,](https://github.com/swaywm/sway/issues/4882#issuecomment-611464474) this is a sway config file for adding icons in title bars using [Font Awesome](https://fontawesome.com/search?o=r&m=free) and [Nerd Fonts Symbols.](https://www.nerdfonts.com/cheat-sheet)

Normally, this is very tedidous to do; so to not waste time on a grand scale with everyone manually trying to specifiy an icon for each app, I decided to make this repo as a shortcut for people who are interested.

# Usage

1. Install Font Awesome.

Arch-based:
```
sudo pacman -S ttf-font-awesome
```

Debian-based:
```
sudo apt install fonts-font-awesome
```

Every other distro: https://fontawesome.com/download

2. Install Nerd Fonts Symbols.

Arch-based:
```
sudo pacman -S ttf-nerd-fonts-symbols
```

Every other distro: https://github.com/ryanoasis/nerd-fonts/releases

3. Clone the repo to `~/.config/sway/`
```
cd ~/.config/sway/
git clone https://github.com/iguanajuice/sway-font-awesome
```

4. Add lines...
```
# Enable title bar icons
exec cd ~/.config/sway/sway-font-awesome && git reset --hard && git pull
include sway-font-awesome/icons
```
...to `~/.config/sway/config`

5. Enable pango in sway's config:
```
font pango:YourChoiceOfFont [font_size]
```

# Contribution

If there are any apps that I haven't added an icon for yet; please open an issue with the `app_id` or `class` of the application that's missing an icon.

You can find the app_id/class by launching the app and running `swaymsg -t get_tree` in a terminal.

Things to know before contributing:
* Be sure to update icons by relogging in before opening any issues.
* Everything should be sorted alphabetically.
* `app_id` and `class` entries should stay seperated.
* Icon should be from Font Awesome primarily; only use Nerd Fonts Symbols if FA has nothing better.
* Icon should be wrapped in \<span size='100%' font-weight='normal'> and \</span> tags.
* Inbetween the icon and \</span> there must be 2 spaces.
* Due to a bug in god knows where, the first \<span> tag must be preceded by a soft-hyphen. You can type this special character by pressing Ctrl+Shift+u, typing "ad", and then pressing enter.
* If an icon is rendered too small, increase size to either 110%, 120%, 133%, or 150%. Icons should be consistent sizes to one another.
* If an icon is placed too high, use `rise='-1pt'` to lower it.
