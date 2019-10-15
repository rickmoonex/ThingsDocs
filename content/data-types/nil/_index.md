---
title: "Nil"
date: 2019-10-14T09:39:58+02:00
weight: 7
---

Probably the most simple type, it can be used as *no value*.

It might be useful to use `nil` as the last statement in a query to prevent
returning data which is not required. See the code example.

> This code uses `nil` to prevent returning unused data:

```
my_array = [1, 2, 3, 42];
nil;  /* without nil, the array above would be returned */
```