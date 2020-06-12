---
title: "emit"
weight: 89
---

Emit an event to all watchers of a [thing](..).
The event is a string value which you are free to choose. It is possible, but not required, to send extra arguments with the event.

{{% notice note %}}
When you emit an event, the event is handled by ThingsDB just as any other event and thus the order in which they are send
to the client is guaranteed.
{{% /notice %}}

This function generates an [event](../../../overview/events).


Using events enables a user to write code like this example of a ChatRoom in the Python language:

```python
class ChatRoom(Thing):
    @event('message/new')
    def on_new_message(self, msg):
        pass  # do something with the message
```

### Function

*thing*.`emit(event, ...)`

### Arguments

Argument | Type | Description
-------- | ---- | -----------
event | str (required) | Event name to emit.
... | any (optional) | Arguments send together with the event.


### Return value

None

### Example

> This code shows an example using ***emit()***:

```thingsdb,json_response
.emit('new/message', 'Hello Everyone!');
```

> Return value in JSON format

```json
null
```