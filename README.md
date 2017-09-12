# Flex

A [Pelican](http://blog.getpelican.com/) theme based on [https://github.com/alexandrevicenzi/Flex/](https://github.com/alexandrevicenzi/Flex/).

## Features

- Mobile First
- Responsive
- Semantic
- SEO Best Practices
- Open Graph
- Rich Snippets (JSON-LD)
- Related Posts (via [plugin](https://github.com/getpelican/pelican-plugins/tree/master/related_posts))
- Minute read like [Medium](https://medium.com/) (via [plugin](https://github.com/getpelican/pelican-plugins/tree/master/post_stats)) (new in 2.0)
- Syntax Highlight with [Prism.js](http://prismjs.com/)
- As an alternative: [Multiple Code Highlight Styles](https://github.com/alexandrevicenzi/Flex/wiki/Code-highlight-support)
- [Translation Support](https://github.com/alexandrevicenzi/Flex/wiki/Translation-support) (new in 2.0)

## Integrations

- [AddThis](http://www.addthis.com/)
- [Disqus](https://disqus.com/)
- [Gauges](http://get.gaug.es/)
- [Google AdSense](https://www.google.com.br/adsense/start/) (new in 2.1)
- [Google Analytics](https://www.google.com/analytics/web/)
- [Google Tag Manager](https://www.google.com/tagmanager/)
- [Piwik](http://piwik.org/)
- [StatusCake](https://www.statuscake.com/)

## Advanced favicon

Theme favours favicon created w/ [RealFaviconGenerator](http://realfavicongenerator.net/).
Webapp creates a zip file w/ multiple resources for different devices and browsers.

Necessary static metadata added (on top of *pelican basics*) to template base.html:

```bash
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
<link rel="icon" type="image/png" href="/favicon-32x32.png" sizes="32x32">
<link rel="icon" type="image/png" href="/favicon-16x16.png" sizes="16x16">
<link rel="manifest" href="/manifest.json">
<link rel="mask-icon" href="/safari-pinned-tab.svg" color="#5bbad5">
```
Chech the previous and adjust as necessary based on info on output of **RealFaviconGenerator**.

Add the following to pelicanconf.py:

```python
FAVICON = SITEURL + '/favicon.ico'

STATIC_PATHS = ['images',
                'static/favicon.ico',
                'static/android-chrome-192x192.png',
                'static/android-chrome-512x512.png',
                'static/apple-touch-icon.png',
                'static/browserconfig.xml',
                'static/favicon-16x16.png',
                'static/favicon-32x32.png',
                'static/manifest.json',
                'static/mstile-150x150.png',
                'static/safari-pinned-tab.svg']

EXTRA_PATH_METADATA = {
    'static/favicon.ico': {'path': 'favicon.ico'},
    'static/android-chrome-192x192.png': {'path': 'android-chrome-192x192.png'},
    'static/android-chrome-512x512.png': {'path': 'android-chrome-512x512.png'},
    'static/apple-touch-icon.png': {'path': 'apple-touch-icon.png'},
    'static/browserconfig.xml': {'path': 'browserconfig.xml'},
    'static/favicon-16x16.png': {'path': 'favicon-16x16.png'},
    'static/favicon-32x32.png': {'path': 'favicon-32x32.png'},
    'static/manifest.json': {'path': 'manifest.json'},
    'static/mstile-150x150.png': {'path': 'mstile-150x150.png'},
    'static/safari-pinned-tab.svg': {'path': 'safari-pinned-tab.svg'}
}
```

## Install

Clone this repo to your local development environment and call from `pelicanconf.py` like `THEME = '../flex'`, relative to your directory setup.

## Development

Install required Node modules with `npm install` (package.json).

After changes, less > min.css with `gulp less`. See `gulpfile.js` for more.

## Translate

Translate this theme to new languages at [Transifex](https://www.transifex.com/alexandrevicenzi/flex-pelican/).

![Translations](https://github.com/alexandrevicenzi/Flex/blob/master/translation_chart.png)

Read more about [Translation Support](https://github.com/alexandrevicenzi/Flex/wiki/Translation-support).

## Prism.js tweaks

This theme uses [Prism.js](http://prismjs.com/) for syntax highlight. Theme is Okaidia, and the following plugins are included:

- Line Numbers
- Copy to Clipboard Button

After downloading, there are couple of things necessary to modify in `prism.css`:

### Fix line height issue for Line Numbers

Add `line-height: 1.2em;` in selector `pre.line-numbers`.

### Change background color of code bocks

Change `background: #272822;` to `background: #333;` in selector `:not(pre) > code[class*="language-"], pre[class*="language-"]`.`

Minify the css with `gulp prism-css` and uglify the js with `gulp prism-js`.

## Docs

[Go to Wiki](https://github.com/alexandrevicenzi/Flex/wiki)

## Contributing

Always open an issue before sending a PR. Talk about the problem/feature that you want to fix. If it's really a good thing you can submit your PR. If you send an PR without talking about before what it is, you may work for nothing.

As always, if you want something that only make sense to you, just fork Flex and start a new theme.

## Live example

I'm using Flex on my [personal website](http://janikarhunen.fi/).

## License

MIT
