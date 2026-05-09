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
    "code2": "zh",
    "code3": "zho",
    "name": "Chinese",
    "nativeName": "中文"
  }
]
```

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `code2` | `string` | Yes | ISO 639-1 language code (2 lowercase letters), e.g. `zh`. |
| `code3` | `string` | Yes | ISO 639-3 language code (3 lowercase letters), e.g. `zho`. |
| `name` | `string` | Yes | English language name. |
| `nativeName` | `string` | Yes | Native/self language name. |

## Translations

Translations are stored in `/translations`, one file per locale (for example: `/translations/zh-CN.json`, `/translations/fr.json`). English is stored directly in `data.json`.

Each translation file has this structure:

```json
{
  "zh": {
    "name": "Chinese"
  }
}
```
