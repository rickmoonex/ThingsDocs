---
title: "add"
date: 2019-10-14T09:56:25+02:00
weight: 1
---

Adds new thing to the [set](../../data-types/set-type) and returns the number of things which are
actually added to the set. For example `my_set.add(#42);` will return `0`
if `my_set` already contains thing `#42`.

This function generates an [event](../../events).

### Function
*set*.`add(thing1, thing1, ..., thingX)`

### Return value
Returns the number of `things` which are added to the set.

> This code adds things to a set:

```
s = set(); a = {item: 'a'}; b = {item: 'b'};
s.add(a, a, b);
```

> Return value in JSON format

```json
2
```