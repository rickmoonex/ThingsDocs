---
title: "user_info"
weight: 163
---

Returns information about a user. If no argument is given, this method will return
information about the current logged in user.

{{% notice note %}}
This function requires `GRANT` privileges on the `@thingsdb` scope when a `username`
other then the logged in user is given as argument. For the currently logged in user, `READ`
privileges on the `@thingsdb` scope are sufficient.
{{% /notice %}}

This function does *not* generate an [event](../../overview/events).

### Function

`user_info([username]);`

### Arguments

Argument | Type | Description
--------- | ----------- | -----------
username | str (optional) | Name of the user

### Return value

Returns [info](../../data-types/info) about the user.

### Example

> This code returns info for the authenticated user:

```thingsdb,should_pass,@t
// Without a `username`, info about the currently logged in user is returned
user_info();
```

> Example output in JSON format:

```
{
    "access": [
        {
            "privileges": "FULL",
            "scope": "@node"
        },
        {
            "privileges": "FULL",
            "scope": "@thingsdb"
        },
        {
            "privileges": "FULL",
            "scope": "@collection:stuff"
        }
    ],
    "has_password": true,
    "name": "admin",
    "tokens": [
        {
            "expiration_time": "2020-11-17 09:25:36Z",
            "key": "QpVmHOsfQaKKpjpOkW0SUt",
            "status": "OK"
        }
    ],
    "user_id": 1
}
```