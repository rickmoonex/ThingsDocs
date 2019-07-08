## user

> This code returns info for the connected user:

```python
import asyncio
from thingsdb.client import Client, scope

async def example():
    await client.connect('node.local')
    client.authenticate(auth=['admin', 'pass'])
    res = await client.query(r'''
        user();
    ''', target=scope.thingsdb)
    print(res)

client = Client()
asyncio.get_event_loop().run_until_complete(example())
```

```shell
thingscmd -n node.local -u admin -p pass -q << EOQ "
user();
"
EOQ
```

> Example return value in JSON format

```json
{
    "access": [
        {
            "privileges": "FULL",
            "target": ":node"
        },
        {
            "privileges": "FULL",
            "target": ":thingsdb"
        },
        {
            "privileges": "FULL",
            "target": "stuff"
        }
    ],
    "name": "admin",
    "tokens": [],
    "user_id": 1
}
```

Returns access and token information about a user.

Without arguments, this function returns info about the connected user and in this case `READ` privileges on the `:thingsdb` scope are sufficient.
If used with a user argument, then this function requires `GRANT` privileges on the `:thingsdb` scope since it exposes user access and token information.

This function does *not* generate an [event](#events).

### Function
`user([username])`

### Arguments
Argument | Type | Description
-------- | ---- | -----------
username | raw/int (optional) | User to return info

### Return value
Information about a ThingsDB user.