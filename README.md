# Flex

A minimalist [Pelican](http://blog.getpelican.com/) theme forked from [https://github.com/alexandrevicenzi/Flex/](https://github.com/alexandrevicenzi/Flex/).

## Features

- Mobile First
- Responsive
- Semantic
- SEO Best Practices
- Open Graph
- Rich Snippets (JSON-LD)
- Syntax Highlight with [Prism.js](http://prismjs.com/)
- Font Awesome icons

## Integrations

- [AddThis](http://www.addthis.com/)
- [Disqus](https://disqus.com/)
- [Gauges](http://get.gaug.es/)
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

Clone this repo to your local development environment and call from `pelicanconf.py` like `THEME = '../../../flex'`.

## Docs

[Go to Wiki](https://github.com/alexandrevicenzi/Flex/wiki)

## Contributing

Always open an issue before sending a PR. Talk about the problem/feature that you want to fix. If it's really a good thing you can submit your PR. If you send an PR without talking about before what it is, you may work for nothing.

As always, if you want something that only make sense to you, just fork Flex and start a new theme.

## Live example

I'm using Flex in my [personal blog](http://janikarhunen.fi/).

Or you can take a look at other [Flex users](https://github.com/alexandrevicenzi/Flex/wiki/Flex-users).

## License

MIT
