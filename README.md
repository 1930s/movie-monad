![Movie Monad](https://i.imgur.com/Vt9Bipy.png)

# Movie Monad

A desktop video player built with Haskell that uses GStreamer and GTK+.

## Screenshots

![GUI showing Sintel from the Blender Foundation](https://i.imgur.com/SLse3s9.jpg)

## Documentation

[Let's make a GTK Video Player with Haskell](https://lettier.github.io/posts/2017-08-30-haskell-gtk-video-player.html)

## Install

### GitHub

```bash
# Install Git
# Install XQuartz (https://www.xquartz.org/) if using Mac OSX or macOS
# Install GTK+ 3.* (https://www.gtk.org/download/index.php)
# Install Haskell
# Install Haksell Stack
# Install ExifTool
git clone https://github.com/lettier/movie-monad.git
cd movie-monad/
stack setup
stack install haskell-gi
haskell-gi -o lib/gi-gdkx11/GdkX11.overrides -O lib/gi-gdkx11 GdkX11-3.0
haskell-gi -o lib/gi-xlib/xlib.overrides     -O lib/gi-xlib xlib
git checkout -- lib/gi-xlib/gi-xlib.cabal
git checkout -- lib/gi-gdkx11/gi-gdkx11.cabal
stack install --dependencies-only
stack build
stack install
stack exec -- movie-monad
```

## License

See [LICENSE](LICENSE).

## Copyright

(C) 2017 David Lettier  
[lettier.com](http://www.lettier.com/)
