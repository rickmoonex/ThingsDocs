---
title: "try"
weight: 128
---

Try a statement and if the statement fails with an error, then the error is returned.
It is also possible to *catch* only specific [errors](../../errors).

{{% notice warning %}}
It is possible to catch all errors with the exception of *internal errors*.
Such errors should never happen, unless something is really wrong with at least one node.
{{% /notice %}}

This function does *not* generate an [event](../../overview/events).

### Function

`try(statement, [e0, e1, ..., eX])`

### Arguments

Argument | Type | Description
-------- | ---- | -----------
statement | any (required) | The statement to try.
e0, e1, ..., eX | int/raw (optional) | Only catch specific errors, if omitted, catch all errors. Error codes and names are accepted.

### Return value

The value for the specified *statement* or an error if the statement has failed.

### Example

> This code shows some return values for ***try()***:

```thingsdb,json_response
[
    iserr( try( x = (1/0) )),
    iserr( try( (1/0), zero_div_err() )),
];
```

> Return value in JSON format

```json
[
    true,
    true
]
```