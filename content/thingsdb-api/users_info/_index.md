---
title: "users_info"
date: 2019-10-14T09:52:04+02:00
weight: 20
---

Returns user information for all users withing ThingsDB.

See the [user_info()](../../thingsdb-api/user_info) function documentation for an example of the exposed user information.

This function requires `GRANT` privileges on the `.thingsdb` scope since it
exposes user access and token information.

This function does *not* generate an [event](../../events).

### Function
`users_info()`

### Arguments
None

### Return value
Array as `qpack` type containing user information for all users within ThingsDB.