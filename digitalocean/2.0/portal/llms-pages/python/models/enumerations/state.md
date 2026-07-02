# State

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXRl

A string representing the current state of the certificate. It may be `pending`, `verified`, or `error`.


# Enum Type Name

`State`


# Fields

| Name |
|  --- |
| `PENDING` |
| `VERIFIED` |
| `ERROR` |


# Example

```python
from digitaloceanapi.models.state import State

state = State.ERROR
```



