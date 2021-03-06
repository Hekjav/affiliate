# Affiliate
Affiliate is a platform agnostic link affiliator. Simplify affiliating links with automatic affiliation in the browser. Affiliate works with libraries that mutate the DOM after the page loads, including React.

[![&#x1f31f; Star me on Github](https://img.shields.io/github/stars/teamtofu/affiliate.svg)](https://github.com/teamtofu/affiliate) [![Download via NPM](https://img.shields.io/npm/dt/affiliate.svg)](https://www.npmjs.com/package/affiliate) [![Bundle small when minified](https://img.shields.io/bundlephobia/min/affiliate.svg)](https://www.npmjs.com/package/affiliate) [![Bundle small when minified and gunzipped](https://img.shields.io/bundlephobia/minzip/affiliate.svg)](https://www.npmjs.com/package/affiliate)

## Installation

```bash
$ npm i -S affiliate
$ yarn add affiliate
```

Or use a CDN
```html
<!-- Replace <VERSION> with your intended version, e.g. 1.2.1 -->
<script src="https://cdn.jsdelivr.net/npm/affiliate@<VERSION>/dist/affiliate.js"></script>
```

## What It Can Do

Affiliate can modify the following link into any of the others.
```html
<a href="https://example.com/shop/product/item-id">Original</a>
```

```html
<a href="https://example.com/shop/product/item-id?ref=my-tag">New Query Tags</a>
<a href="https://example.com/shop/product/item-id/ref/my-tag">Modified URL Path</a>
<a href="https://my-tag.example.com/shop/product/item-id">Modified Host Name</a>
```

Affiliate has easy [plugins](https://affiliate.js.org/plugins), including one for [Amazon](https://affiliate.js.org/plugins/amazon), which simplify adding affiliate links even more.

## Basic Setup

Read [the documentation](https://affiliate.js.org/) for more advanced usage.

```js
const Affiliate = require('affiliate');
const aff = Affiliate({
    tags: [
        {
            hosts: ['example.com', 'www.example.com'],
            query: {
                ref: 'my-tag' // This means ?ref=my-tag
            }
        },
        {
            hosts: ['example.org', 'shop.example.org'],
            query: {
                tag: 'my-tag2' // This means ?tag=my-tag2
            }
        }
    ]
});
aff.attach();
```

## Documentation

Affiliate is simple and quick to set up, even for more complex usage. Read the docs at: [affiliate.js.org](https://affiliate.js.org/).

### Blogs and Related Sites

A simplified codeless solution might better suit some blogging-style sites.

Insert this code into the page `<head>`. The contents of the `data-aff` attribute will tell Affiliate what to do.
```html
<!-- Replace 1.2 with your intended version -->
<script data-aff="amazon.com, www.amazon.com : tag = MY-AMAZON-TAG" src="https://cdn.jsdelivr.net/npm/affiliate@1.2/dist/affiliate.js" async id="aff-js"></script>
```

#### data-aff Syntax
The syntax for data-aff is a comma separated list of domains, a colon, and then comma separated list of url queries in the format `key=value`. Multiple website groups can be separated by an exclamation mark.
```
amazon.com, www.amazon.com : tag = MY-AMAZON-TAG ! example.com, shop.example.com : ref = MY-OTHER-TAG
```

## Testing

Affiliate is tested using Jasmine. The test of the minified packages is available [here](https://affiliate.js.org/test/index.html) and the webpack package [here](https://affiliate.js.org/test/webpack.html).

### Big Thanks

[![Sauce Labs](https://affiliate.js.org/test/sauce/saucelabs.png)](https://saucelabs.com/)

Cross-browser Testing Platform and Open Source <3 Provided by [Sauce Labs](https://saucelabs.com/)!

## Star This Project

If you like it then you gotta [put a star on it](https://github.com/teamtofu/affiliate). &#x1f609;&#x1f31f;

## License

MIT (C) [Russell Steadman](https://teamtofu.github.io/contact/). Learn more in the [LICENSE](https://github.com/teamtofu/affiliate/blob/master/LICENSE) file.

## Support Me

Like this project? Buy me a [cup of coffee](https://www.paypal.me/RussellSteadman/3). &#x2615; Here are more of my [projects](https://teamtofu.github.io/).