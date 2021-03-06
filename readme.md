# is-absolute-url [![Build Status](https://travis-ci.org/sindresorhus/is-absolute-url.svg?branch=master)](https://travis-ci.org/sindresorhus/is-absolute-url)

> Check if a URL is absolute

By default, it checks if the URL uses the `http` or `https` protocol.


## Install

```
$ npm install is-absolute-url
```


## Usage

```js
const isAbsoluteUrl = require('is-absolute-url');

isAbsoluteUrl('https://sindresorhus.com/foo/bar');
//=> true

isAbsoluteUrl('http://sindresorhus.com/foo/bar');
//=> true

isAbsoluteUrl('ftp://sindresorhus.com/foo/bar');
//=> false

isAbsoluteUrl('ftp://sindresorhus.com/foo/bar', {httpOnly: false});
//=> true

isAbsoluteUrl('//sindresorhus.com');
//=> false

isAbsoluteUrl('foo/bar');
//=> false
```

By default only `http` and `https` links are validated.  If you wish to check absolute URLs of protocols other than `http` (for example, `ftp:`, `mailto:`), use `isAbsoluteUrl(mayBeURL, { httpOnly: false })`.

## API

### isAbsoluteUrl(url, options?)

#### url

Type: `string`

The URL to be checked.

#### options

Type: `object`

##### httpOnly

Type: `boolean`\
Default: `true`

Set to `false` if the url does not use `http`/`https` protocol.

## Related

See [is-relative-url](https://github.com/sindresorhus/is-relative-url) for the inverse.


---

<div align="center">
	<b>
		<a href="https://tidelift.com/subscription/pkg/npm-is-absolute-url?utm_source=npm-is-absolute-url&utm_medium=referral&utm_campaign=readme">Get professional support for this package with a Tidelift subscription</a>
	</b>
	<br>
	<sub>
		Tidelift helps make open source sustainable for maintainers while giving companies<br>assurances about security, maintenance, and licensing for their dependencies.
	</sub>
</div>
