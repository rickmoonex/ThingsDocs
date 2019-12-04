---
title: "type_count"
weight: 130
---

Returns the number of instances of a given [Type](../../data-types/type) within a collection.

This function does *not* generate an [event](../../overview/events).

### Function

`type_count(type_name)`

### Arguments

Argument | Type | Description
-------- | ---- | -----------
type_name | str | The name of the Type for which the number of instances must be returned.

### Return value

An `int` representing the number of occurrences.