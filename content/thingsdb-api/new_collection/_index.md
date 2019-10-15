---
title: "new_collection"
date: 2019-10-14T09:49:59+02:00
weight: 8
---

Create a new collection.

This function generates an [event](../../events).

### Function
`new_collection(name);`

### Arguments
Argument | Type | Description
--------- | ----------- | -----------
name | raw (required) | Name of the new collection.

{{% notice note %}}
The user who has created the collection will automatically receive full
access rights to the new collection.
Use `grant` to give other users access to the collection.
{{% /notice %}}

### Return value
Returns the new collection `id` if successful. An `INDEX_ERROR` is raised
if the collection already exists.

> This code will create a collection *"awesome_things"*:

```
// Creates a new collection
new_collection('awesome_things');
```

> Example return value in JSON format (the new collection id)

```json
31415
```