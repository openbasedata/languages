# Languages Open Base Data

## How To Use

```bash
npm install @openbasedata/languages
```

`data.json` contains language metadata in English and native representation.

Other localized translations are split into `/translations/<locale>.json` (one language per file) to keep the main dataset smaller.

## Data Structure

```json
[
  {
    "code": "zh",
    "name": "Chinese",
    "nativeName": "中文"
  }
]
```

| Field        | Type     | Required | Description                                               |
| ------------ | -------- | -------- | --------------------------------------------------------- |
| `code`       | `string` | Yes      | ISO 639-1 language code (2 lowercase letters), e.g. `zh`. |
| `name`       | `string` | Yes      | English language name.                                    |
| `nativeName` | `string` | Yes      | Native/self language name.                                |

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
