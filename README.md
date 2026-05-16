# Languages Open Base Data

[![npm version](https://img.shields.io/npm/v/@openbasedata/languages.svg)](https://www.npmjs.com/package/@openbasedata/languages)
[![npm downloads](https://img.shields.io/npm/dm/@openbasedata/languages.svg)](https://www.npmjs.com/package/@openbasedata/languages)

## How To Use

```bash
npm install @openbasedata/languages
```

`data.json` contains language metadata in English and native representation, etc.

Other localized translations are split into `/translations/<locale>.json` (one language per file) to keep the main dataset smaller.

## Data Structure

```json
[
  {
    "code": "zh",
    "name": "Chinese",
    "nativeName": "中文",
    "population": 0
  }
]
```

| Field        | Type     | Required | Description                                                 |
| ------------ | -------- | -------- | ----------------------------------------------------------- |
| `code`       | `string` | Yes      | ISO 639-1 language code (2 lowercase letters), e.g. `zh`.   |
| `name`       | `string` | Yes      | English language name.                                      |
| `nativeName` | `string` | Yes      | Native/self language name.                                  |
| `population` | `number` | Yes      | Estimated speaker population (`0` when no estimate exists). |

## Translations

Translations are stored in `/translations`, one file per locale (for example: `/translations/zh-Hans.json`, `/translations/fr.json`). English is stored directly in `data.json`.

Each translation file has this structure:

```json
{
  "zh": {
    "name": "Chinese"
  }
}
```

## Changelog

Generate the changelog from git history with:

```bash
npm run changelog
```

The generated output is written to `/CHANGELOG.md`.
