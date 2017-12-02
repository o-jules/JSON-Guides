# Regular expression matched for JSON values

## string

```re
^"([^"\\]|\\([\"\\/bfnrt]|u\d{4}))*"$
```

## number

```re
^-?(0|[1-9]\d*)(\.\d+)?([eE][+\-]?\d+)?$
```

## literals

```re
(null|true|false)
```
