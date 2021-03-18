# ST Image Background

This is a patch to enable the use of an image background for st (Suckless Terminal)

If patched, starting st will make it look for the image file "wall0" in: $HOME/.config/wall0, to use it as a background. If it doesn't find or can't open the file, the terminal will just use the normal background color.

# File type

wall0 can be any image file supported by the DevIL image library, just take your processed wallpaper (Blurred, darkened...), rename it wall0 and put it in $HOME/.config/
Note that your image must have the same size as your screen, this patch only displays the image, it doesn't process it in any way.

# Dependencies

The only additional dependency compared to vanilla st is DevIL. If you're on Arch Linux, just type :

```shell
sudo pacman -S devil
```

# Live Update

If you want st to update its background image without having to restart it, use this [event emitter](https://github.com/hexoctal/st-bg-event).

You could also use this [script](https://github.com/hexoctal/change-theme) to automatically set a new image as a wallpaper as well as a background for st, and update all open instances of st.
