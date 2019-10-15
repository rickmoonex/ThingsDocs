---
title: "isint"
date: 2019-10-14T10:01:44+02:00
weight: 28
---

This function determines whether the value passed to this function
is an [integer](../../data-types/integer) or not.

This function does *not* generate an [event](../../events).

### Function
`isint(value)`

### Arguments
Argument | Type | Description
-------- | ---- | -----------
value | any (required) | The value to be tested.

### Return value
Returns `true` is the passed value is an integer else it returns `false`.

> This code shows some return values for ***isint()***:

```
[
    isint( 42 ),
    isint( 0x2a ),
    isint( 42.0 ),
    isint( '42' ),
    isint( true ),
];
```

> Return value in JSON format

```json
[
    true,
    true,
    false,
    false,
    false
]
```