## index_err

> This code shows ***index_err()***:

```python
import asyncio
from thingsdb.client import Client

async def example():
    await client.connect('node.local')
    await client.authenticate(auth=['admin', 'pass'])
    res = await client.query(r'''
        index_err()
    ''', target='stuff')
    print(res)

client = Client()
asyncio.get_event_loop().run_until_complete(example())
```

```shell
thingscmd -n node.local -u admin -p pass -c stuff -q << EOQ "
index_err();
"
EOQ
```

> Return value in JSON format

```json
{
    "!": "index_err()",
    "error_code": -54,
    "error_msg": "requested resource not found"
}
```

Returns an [error](#error-type).

This function does *not* generate an [event](#events).

### Function
`index_err([message])`

### Arguments
Argument | Type | Description
-------- | ---- | -----------
message | raw (optional) | Alternative error message.

### Return value
An error value.