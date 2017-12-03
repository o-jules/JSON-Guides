# Differences between JSONs and JavaScript object/dictionary literals

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

JSON values human-readability. So it is agnostic about number formats.

  - Extra positive sign is not neeeded, `+1` is invalid.
  - Redudant `0`s in head is considered invalid, thus `001`, `00.1` are all invalid in JSON;
  - Numbers must be decimal system; not hexadecimal or others, thus, `0x01` is in valid in JSON;
