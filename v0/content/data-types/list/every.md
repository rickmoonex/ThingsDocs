---
title: "every"
weight: 38
---

This function tests whether all elements in the array pass a given test. It returns a [boolean](../../bool) value.

{{% notice info %}}
Calling this function on an empty array returns `true` for any condition!
{{% /notice %}}


This function does *not* generate an [event](../../../overview/events).

### Function

*array*.`every(callback)`

### Arguments

Argument | Type | Description
-------- | ---- | -----------
callback | closure | Closure to execute on each value until the closure evaluates to false.

Explanation of the *callback* argument:

Iterable | Arguments   | Description
-------- | ----------- | -----------
array    | item, index | Iterate over items in the array. Both `item` and `index` are optional.

### Return value

Returns `true` if the callback function returns a *truthy* value for every array element. Otherwise, `false`.

### Example

> This code shows an example using ***find()***:

```thingsdb,json_response
a = [12, 5, 8, 130, 44].every(|x| x >= 10);   // false
b = [12, 54, 18, 130, 44].every(|x| x >= 10); // true

// Return both a and b
[a, b];
```

> Return value in JSON format

```json
[
    false,
    true
]
```