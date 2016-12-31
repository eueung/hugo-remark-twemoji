# hugo-remark-twemoji
This template is for authoring remark slides featuring conversational (Tw)emoji within Hugo.

[Remark](https://github.com/gnab/remark) is a flexible and powerful HTML presentation framework which renders nicely markdown content. This project is an attempt to manage content entirely with Hugo, featuring [Twitter Emoji (Twemoji)](http://twitter.github.io/twemoji/) conversational templates.

Preview of the available twemoji can be seen [here](http://twitter.github.io/twemoji/2/test/preview.html). This project utilizes [twemoji-awesome](https://github.com/ellekasai/twemoji-awesome) CSS interface. Emoji names are mostly (claimed) to be compatible with [Emoji cheat sheet](http://www.webpagefx.com/tools/emoji-cheat-sheet/).

![Screenshot](https://raw.githubusercontent.com/eueung/hugo-remark-twemoji/master/images/screenshot.png)

## Demo

- [Official Remark Slides + Twemoji](//eueung.github.io/hugo-remark-twemoji/)

## Installation

Inside the folder of your Hugo site run:

    $ cd themes
    $ git clone https://github.com/eueung/hugo-remark-twemoji.git remark-twemoji

For more information read the official [setup guide](//gohugo.io/overview/installing/) of Hugo.

## Sample Configuration

The following `config.toml` is used for the demo site mentioned above.

```toml
baseurl         = "/"
theme           = "remark-twemoji"
languageCode    = "en-us"
title           = "Site Title | Hugo Remark-Twemoji"
canonifyurls    = true

[params]
  googleAnalytics = ""
  name            = "Eueung Mulyana"
  description     = "Demo slides for Hugo Remark Twemoji"
  custom_css      = ["custom.css"]
```

## Sample Content

Sample content structure is given in the `exampleSite` folder. Because of the current (v0.18) implementation of `.RawContent` which does not render Hugo shortcode, page variable `contentType` must be set to `sc` (abbreviated shortcode), otherwise it has to be set to `md` (markdown). The above screenshot was produced with the following source.

```
+++
contentType = "sc"
weight = 26
+++

{{< twemoji_right title="#Learn" emoji="owl" >}}
Always learn something new ..
{{< /twemoji_right >}}
```
## Sample Style

Usually you'll maintain your own custom CSS. This has to be declared in the `config.toml`. Sample style is included in the `exampleSite/static/css` folder.

Have fun!

## License

This theme is released under the MIT license. For more information read the [License](//github.com/eueung/hugo-remark-twemoji/blob/master/LICENSE.md).

