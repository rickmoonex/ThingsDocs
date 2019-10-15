---
title: "isbool"
date: 2019-10-14T10:00:44+02:00
weight: 24
---

This function determines whether the value passed to this function
is a [bool](../../data-types/boolean) or not.

This function does *not* generate an [event](../../events).

### Function
`isbool(value)`

### Arguments
Argument | Type | Description
-------- | ---- | -----------
value | any (required) | The value to be tested.

### Return value
Returns `true` is the passed value is a boolean else it returns `false`.

> This code shows some return values for ***isbool()***:

```
[
    isbool( true ),
    isbool( 'true' ),
    isbool( nil ),
];
```

> Return value in JSON format

```json
[
    true,
    false,
    false
]
```