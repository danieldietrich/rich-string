[![npm version](https://img.shields.io/npm/v/@danieldietrich/rich-string?logo=npm&style=flat-square)](https://www.npmjs.com/package/@danieldietrich/rich-string/)[![vulnerabilities](https://img.shields.io/snyk/vulnerabilities/npm/@danieldietrich/rich-string?style=flat-square)](https://snyk.io/test/npm/@danieldietrich/rich-string)[![minzipped size](https://img.shields.io/bundlephobia/minzip/@danieldietrich/rich-string?style=flat-square)](https://bundlephobia.com/result?p=@danieldietrich/rich-string@latest)
&nbsp;
[![build](https://img.shields.io/travis/danieldietrich/rich-string?logo=github&style=flat-square)](https://travis-ci.org/danieldietrich/rich-string/)[![coverage](https://img.shields.io/codecov/c/github/danieldietrich/rich-string?style=flat-square)](https://codecov.io/gh/danieldietrich/rich-string/)
&nbsp;
![Platform](https://img.shields.io/badge/platform-Node%20v10%20%20+%20Browser%20%28ES6%2fES2015%29-decc47?logo=TypeScript&style=flat-square)
&nbsp;
[![donate](https://img.shields.io/badge/Donate-PayPal-blue.svg?logo=paypal&style=flat-square)](https://paypal.me/danieldietrich13)[![patrons](https://img.shields.io/liberapay/patrons/danieldietrich?style=flat-square)](https://liberapay.com/danieldietrich/)[![license](https://img.shields.io/github/license/danieldietrich/rich-string?style=flat-square)](https://opensource.org/licenses/MIT/)
&nbsp;
[![Follow](https://img.shields.io/twitter/follow/danieldietrich?label=Follow&style=social)](https://twitter.com/danieldietrich/)

# rich-string

A tag function that automatically aligns embedded multiline strings.

## Installation

```bash
npm i @danieldietrich/rich-string
```

## Usage

The module supports ES6 _import_ and CommonJS _require_ style.

```ts
import s from '@danieldietrich/rich-string';

/*
function sayHi(name) {
    console.log('Hi ${name}, I hope you are doing well!');
}
*/
const res = generateSayHi(s`

    console.log('Hi \${name}, I hope you are doing well!');

`);

function generateSayHi(body: string): string {
    return s`
        function sayHi(name) {
            ${body}
        }
    `;
}
```

---

Copyright &copy; 2019 by [Daniel Dietrich](cafebab3@gmail.com). Released under the [MIT](https://opensource.org/licenses/MIT/) license.