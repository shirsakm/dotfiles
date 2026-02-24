# These are my dotfiles!

This is just a collection of my personal configuration files and wallpapers, as well as other random bits and bobs that help when setting up a new environment.
And version control ain't ever hurt nobody!

If you wish to use these dotfiles as well, beware that these were tested and are currently being used on XFCE, and your mileage may vary if you aren't using XFCE as well.
Barring that warning, all you need to know is that this repo is managed using [GNU Stow](https://www.gnu.org/software/stow/). If the folders look wonky, that's why!

If you know how to use Stow already, go right ahead, if not, here is a quick introduction.

## Why are you using Stow?

In layman's terms, as used here, it creates symlinks between the actual config folder and this dotfiles repository.
The symlink, however, is backwards, because adding symlinks to the repository would not be the most productive use of my time.

It has other uses of course, but that further reading is left as an exercise to the reader.

## That's great, but how do I actually use this?

Great question!

1. Firstly you will need to install `stow` as a package on your distribution.
2. Clone the repository (or download an archive of it, if you are lame).
3. Run `stow` in the dotfiles directory:
```sh
# this creates symlinks for every single component
stow */
```

If you don't need all the config files, and want only a partial set of the files, you can also run stow on a component basis:
```sh
# this creates symlink only for the specified module e.g. stow kitty/ would only copy over the Kitty config files
# replace kitty/ with whatever config directory you want to symlink together
stow kitty/
```

To remove a configuration, simply use the delete flag:
```sh
stow -D kitty
```
