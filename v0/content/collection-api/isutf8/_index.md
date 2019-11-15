---
title: "isutf8"
date: 2019-10-14T10:03:04+02:00
weight: 25
---

This function determines whether the value passed to this function is of
type `raw` and contains valid utf8.

This function does *not* generate an [event](../../events).

### Function

`isutf8(value)`

### Arguments

Argument | Type | Description
-------- | ---- | -----------
value | any (required) | The value to be tested.

### Return value

Returns `true` is the given value is of type `raw` and contains valid utf8, else `false`.

> This code shows some return values for ***isutf8()***:

```thingsdb,json_response
[
    isutf8( 'ԉ' ),
    isutf8( 'pi' ),
];
```

> Return value in JSON format

```json
[
    true,
    true
]
```
