---
title: "istuple"
date: 2019-10-14T10:02:50+02:00
weight: 36
---

This function determines whether the value passed to this function
is a immutable [array](../../data-types/array-type) or not. At least nested arrays are of kind tuple.

This function does *not* generate an [event](../../events).

### Function
`istuple(value)`

### Arguments
Argument | Type | Description
-------- | ---- | -----------
value | any (required) | The value to be tested.

### Return value
Returns `true` is the passed value is a tuple else it returns `false`.

> This code shows some return values for ***istuple()***:

```
[
    istuple( [] ),
    istuple( tmp = [['nested'], set()] ),
    istuple( tmp[0] ),
    istuple( tmp[1] ),
];
```

> Return value in JSON format

```json
[
    false,
    false,
    true,
    true
]
```