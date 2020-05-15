# JSON v.s. JavaScript values

The grammar structure of JSON is less complex than JavaScript object literals. Because JSON is designed for data exchange, serialization and deserialization would be frequently. A simple scheme and exclusion of language specific features is the way to go.

## Types

Those types are allowed in JSON only:
  - String
  - Number
  - Object
  - Array
  - Boolean: `true`, `false`
  - `null`

Thus, literals like `undefined` and `Infinity` are all invalid.

## Comments

Comments are not supported. Neither `//` nor `/* */`.

## Keys

The keys are strings. The rules apply to **String** also apply to the keys.

## Comma

Dangling tail comma is not allowed, thus:
```json
{
  a: 1,
  b: 1,
}
```
The final comma is invalid.

## Strings

Strings must be wrapped by *doubled quotes `"`*; Strings starting with *single quotes `'`* and *grave accent `\``*(string interpolation) are invalid.

## Numbers

- Format

  JSON values human-readability. So it is agnostic about number formats.

  - Extra positive sign in JSON is not invalid, e.g. `+1`.
  - Redudant `0`s in head is considered invalid, thus `001`, `00.1` are all invalid in JSON;
  - Numbers must be decimal system; not hexadecimal or others, thus, `0x01` is in valid in JSON;

- Precision

  JSON spec has no limit in number precisions, while JavaScript does.

  Conversion from JSON to JavaScript may cause precision loss in number.