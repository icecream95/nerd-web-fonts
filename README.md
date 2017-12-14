# nerd-web-fonts

[**Nerd** Web Fonts](https://github.com/ryanoasis/nerd-fonts) working in [Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo) and working also on **Chromebook** (or pretty much anything running Chrome).

There are multiple `font-family` to choose from (all Nerd-enabled):

  * `DejaVu Sans Mono, DejaVu Sans Mono Bold` -
    [DejaVu Sans Mono for Nerd](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/DejaVuSansMono)
  * `Hack` -
    [Hack for Nerd](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/Hack)
  * `Roboto Mono` -
    [Roboto Mono for Nerd](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/RobotoMono)
  * `Ubuntu Mono` -
    [Ubuntu Mono for Nerd](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/UbuntuMono)

See [preview.html](https://rawgit.com/icecream95/nerd-web-fonts/master/preview.html) and [Slant](http://www.slant.co/topics/67/~programming-fonts) if you don't know which to choose.

## Usage example

### Usage example for [Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo)

  - Options:
      - font-family: `"DejaVu Sans Mono", "DejaVu Sans Mono Bold", monospace`
      - user-css: `TODO`

Note that having both the normal and bold versions of a font is only required for DejaVu Sans Mono, and when it is added, Source Code Pro.

### Usage example for [Crosh Window](https://chrome.google.com/webstore/detail/crosh-window/nhbmpbdladcchdhkemlojfjdknjadhmh)

  - Start crosh window then press `Ctrl+Shift+J` and paste in the following:

```js
term_.prefs_.set('font-family', '"DejaVu Sans Mono", "DejaVu Sans Mono Bold", monospace');
term_.prefs_.set('user-css', 'TODO');
```

If you have [Crouton](https://github.com/dnschneid/crouton) installed on a developer mode Chromebook,
or if you're on pretty much any other OS, you can install those fonts locally or copy them locally
and it'll work with little to no effort.

## Suggesting a new font

To add a new font, you can submit a GitHub pull request. Your PR should:

  - Include a new font file in [WOFF2
    format](https://gist.github.com/sergejmueller/cf6b4f2133bcb3e2f64a).
  - Add your font to `PowerlineFonts.css`, `preview.html` and `README.md` (might use [Transfonter](http://transfonter.org/) to help with the CSS).

The font should not be the Mono version and should be converted using [Monospacifier](https://github.com/cpitclaudel/monospacifier) of similar for PR's to the master branch, and should be the Mono version for the mono branch.

### Converting to WOFF2

There are various methods, including:

  * [otf to woff2 | Everything Fonts](https://everythingfonts.com/otf-to-woff2)
  * [ttf to woff2 | Everything Fonts](https://everythingfonts.com/ttf-to-woff2)
  * [Webfont Generator | Font Squirrel](https://www.fontsquirrel.com/tools/webfont-generator)
  * Using [FontForge](https://fontforge.github.io/en-US/):

        #!/usr/bin/env fontforge
        Open($1)
        Generate($1:r + ".woff2")`

Thanks to [Wernight's powerline fonts](https://github.com/wernight/powerline-web-fonts) for the base of this project.