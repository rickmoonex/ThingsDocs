---
title: "assert"
date: 2019-10-14T09:56:39+02:00
weight: 3
---

Raises `ASSERTION_ERROR` if the specified statement evaluates to `false`.

This function does *not* generate an [event](../../events).


### Function
`assert(statement [, error_msg])`

### Arguments
Argument | Type | Description
-------- | ---- | -----------
statement | any (required) | The statement to evaluate.
msg | raw (optional) | Custom error message.
code | int (optional) | Return a custom error code between 1 and 32. If not given, the error code is `ASSERTION_ERROR` (-105)

### Return value
Assert returns with the return value of the given statement when the statement evaluates to `true`. Otherwise
an `ASSERTION_ERROR` is raised.

> This code shows how assert can be used:

```
assert(1 > 2, 'one is still smaller than two');
```

> Returns with an  `ASSERTION_ERROR` exception

```json
{
    "error_msg": "one is still smaller than two",
    "error_code": 1
}
```