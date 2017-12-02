# Differences between JSONs and JavaScript object/dictionary literals

## Types

Those types are allowed in JSON only:
  - string
  - number
  - object
  - array
  - Boolean: true, false
  - null

Thus, things like `undefined` and `Infinity` in invalid.

## Comments

Comments are not supported.

## Keys

Keys are strings. The rules apply to string also apply to keys.

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

Strings must be wrapped by *doubled quotes `"`*; Strings starting with *single quotes `'`* and *grave accent `\``* are invalid.

## Numbers

  - Extra positive sign is not neeeded, `+1` is invalid.
  - Redudant `0`s in head is considered invalid, thus `001`, `00.1` are all invalid in JSON;
  - Numbers must be decimal system; not hexadecimal or others, thus, `0x01` is in valid in JSON;

