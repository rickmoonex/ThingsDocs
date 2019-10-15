---
title: "new_user"
date: 2019-10-14T09:50:22+02:00
weight: 11
---

Creates a new user to ThingsDB. The new user is created without a password, token and access privileges.
You probably want to [set a password](../../thingsdb-api/set_password) or add a [new token](../../thingsdb-api/new_token) and assign some privileges using [grant(...)](../../thingsdb-api/grant).

This function generates an [event](../../events).

### Function
`new_user(user);`

### Arguments
Argument | Type | Description
-------- | ---- | -----------
`user` | raw (required) | Username, between 1 and 128 *graphical* characters.

### Return value
Returns the new user `id` if successful. An `INDEX_ERROR` is raised
if the user already exists.

> Create a new user `iris` with password `siri`:

```
new_user('iris');
```

> Example return value in JSON format (the new user id)

```json
19
```