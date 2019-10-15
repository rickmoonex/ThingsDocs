---
title: "del"
date: 2019-10-14T09:57:23+02:00
weight: 8
---

Delete a property from a [thing](../../data-types/thing-type).

This function generates an [event](../../events).

### Function
*thing*.`del(property)`

### Arguments
Argument | Type | Description
-------- | ---- | -----------
property | raw (required) | Name of the property to delete.

### Return value
Returns `nil` if successful. An `INDEX_ERROR` is returned
if the property does not exist or `BAD_REQUEST` in case the given property is
not a valid [name](../../names).

> This code shows some return values for ***del()***:

```
.x = 'create and delete this prop';
.del('x');
```

> Return value in JSON format

```json
null
```