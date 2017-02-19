## What makes this "Swedish colemak" different from Tarrasch@githubs version?

This is copied from [Tarraschs](https://gist.github.com/Tarrasch/1293692#what-makes-this-swedish-colemak) github readme:

>It simply squeezes in `åäö` comfortably on the **home row** through `AltGr`.
>It tries in no way to edit anything else on colemak, so it's still
>optimized for English and not Swedish.
>
>Additionally I've squeezed a lot of other fancy stuff through `AltGr`,
>which are independent of the language.

Since it is based on his template all those things are still true. However,
I found that i could not achieve the same speeds as I could in english due
to the need of a modifier key needed for `åäö`. So this version of 
colemak, **which is intended to be used in conjunction with Tarraschs version**, 
places `öå` right of `y` and `ä` right of `o`. **This makes it tedious to write
`{}` and `[]`.** Therefore I suggest you get both mine and Tarraschs version so
you can switch to his version when coding.

## Manual installation instructions.

This is done on arch, but should work for most systems.

Replacing `Swedish (Dvorak)`

    sudo cp /usr/share/X11/xkb/symbols/se{,-backup}
    wget https://raw.githubusercontent.com/JAnken123/swemak/master/se
    sudo cp se /usr/share/X11/xkb/symbols/se

For the changes to take affect, just log in and out. If you want to avoid the replace,
you can do it the proper way by following these [instructions](https://ubuntuforums.org/showthread.php?t=188761).

But really just replacing one of which you do not use is simpler.

## About this layout:
  `öå` right of `y` 
  `ä` right of `o`


## Feedback

boxymonk@gmail.com

## Typical errors

Caps lock is still activating caps and is also working as backspace.

I myself use gnome atm and this is fixed by using the tweak tool in 
typing under caps lock function. You can also fix it per session 
(could put it in some start-up script) with some instructions. Here is a [link](https://www.howtogeek.com/194705/how-to-disable-or-reassign-the-caps-lock-key-on-any-operating-system/)
on how to do it for all operating systems.

This is the most common setting.

    setxkbmap -option caps:backspace -option shift:both_capslock
