# Bad JSONs parsed by browser

How will browser handle bad JSONs?

The following cases were tested in Chrome only.

## Direct `GET` JSON files

Chrome will show details about the errors in which line and which character position of the JSON file/string.

## `GET` through ajax

There will be identical errors hint as `JSON.parse()`.
