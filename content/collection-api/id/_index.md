---
title: "id"
date: 2019-10-14T09:59:59+02:00
weight: 19
---

Returns the `id` of a [thing](../../data-types/thing-type) or `nil` if the thing is not stored.

This function does *not* generate an [event](../../events).

### Function
*thing*.`id()`

### Arguments
None

### Return value
Returns `id` of a thing or `nil` when the thing is not stored.

> This code uses `id()` to return a collection id:

```
.id();  // Returns the collection id
```

> Example return value in JSON format

```json
3
```