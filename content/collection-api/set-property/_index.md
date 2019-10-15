---
title: "set (property)"
date: 2019-10-14T10:05:11+02:00
weight: 51
---

Creates a new property on a thing. If the property already existed then the old
property will be overwritten. This function is equal to an assignment except that
it can be used when the `name` of the property is dynamic.

This function generates an [event](../../events).

### Function
*thing*.`set(name, value)`

### Arguments
Argument | Type | Description
-------- | ---- | -----------
name | raw (required) | The name of the property to set.
value | any (required)  | The value which will be assigned to the property.

### Return value
The value which will be assigned.

> This code shows how to use ***set()***:

```
.set('the_answer', 42);
```

> Return value in JSON format

```json
42
```