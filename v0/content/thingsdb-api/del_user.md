---
title: "del_user"
weight: 152
---

Delete a user. It is not possible to delete your own user account and a [bad_data_err()](../../errors/bad_data_err) will be raised in case you try to.
Any *tokens* associated with the user will also be deleted.

This function generates an [event](../../overview/events).

### Function

`del_user(username);`

### Arguments

Argument | Type | Description
-------- | ---- | -----------
username | str (required) | Username of the user to delete.

### Return value

Returns `nil` when successful. A [lookup_err()](../../errors/lookup_err) is raised if the user does not exist.

### Example

> This code will delete user *test*:

```thingsdb,syntax_only,@t
// Delete user `test`
del_user('test');
```