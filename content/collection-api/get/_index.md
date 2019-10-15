---
title: "get"
date: 2019-10-14T09:59:34+02:00
weight: 16
---

Return the value of a property on a [thing](../../data-types/thing-type) by a given property name.
If the property is not found then the return value will be `nil`, unless an alternative
return value is given.

This function does *not* generate an [event](../../events).

### Function
*thing*.`get(name [, alt])`

### Arguments
Argument | Type | Description
-------- | ---- | -----------
name | raw (required) | Name of the property where to return the value for.
alt | any (optional) | Optional return value.

### Return value
Returns the value for the given property name. If the property is not found the the
return value will be `nil`  unless an alternative return value is given as second argument.

> This code shows an example use case of ***get()***:

```
tmp = {name: 'Iris'};
tmp.get('name');
```

> Return value in JSON format

```json
"Iris"
```