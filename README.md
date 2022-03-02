# Knex.js types generator

[![NPM Version](https://img.shields.io/npm/v/knex-types?style=flat-square)](https://www.npmjs.com/package/knex-types)
[![NPM Downloads](https://img.shields.io/npm/dm/knex-types?style=flat-square)](https://www.npmjs.com/package/knex-types)
[![TypeScript](https://img.shields.io/badge/%3C%2F%3E-TypeScript-%230074c1.svg?style=flat-square)](http://www.typescriptlang.org/)
[![Donate](https://img.shields.io/badge/dynamic/json?color=%23ff424d&label=Patreon&style=flat-square&query=data.attributes.patron_count&suffix=%20patrons&url=https%3A%2F%2Fwww.patreon.com%2Fapi%2Fcampaigns%2F233228)](http://patreon.com/koistya)
[![Discord](https://img.shields.io/discord/643523529131950086?label=Chat&style=flat-square)](https://discord.gg/bSsv7XM)

An utility module for [Knex.js](https://knexjs.org/) that generates [TypeScript definitions](https://knexjs.org/#typescript-support) (types) from a PostgreSQL database schema.

```
$ npm install knex
$ npm install knex-types --dev
```

## Usage Example

```js
const { knex } = require("knex");
const { updateTypes } = require("knex-types");

const db = knex(require("./knexfile"));

updateTypes(db, { output: "src/types/knex.d.ts" }).catch((err) => {
  console.error(err);
  process.exit(1);
});
```

Find an example of generated types in [`./main.test.ts`](./main.test.ts).

## License

Copyright © 2021-present Kriasoft. This source code is licensed under the MIT license found in the
[LICENSE](https://github.com/imjamesku/knex-types-generator/blob/main/LICENSE) file.

---

<sup>Made with ♥ by Konstantin Tarkus ([@koistya](https://twitter.com/koistya), [blog](https://medium.com/@koistya))
and [contributors](https://github.com/kriasoft/knex-types/graphs/contributors).</sup>
