---
title: "contains"
date: 2019-10-14T09:57:04+02:00
weight: 6
---

Determines if a given string is a substring of a string.

This function does *not* generate an [event](../../events).

### Function
*string*.`contains(search_string)`

### Arguments
Argument | Type | Description
-------- | ---- | -----------
search_string | raw (required) | The characters to be searched for in the string.

### Return value
Returns `true` the given characters are found as a substring and otherwise `false`.

> This code shows an example using ***contains()***:

```
'the answer to life the universe and everything'.contains('life');
```

> Return value in JSON format

```json
true
```