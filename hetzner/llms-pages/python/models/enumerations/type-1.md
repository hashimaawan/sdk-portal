# Type 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlR5cGUx

Choose between uploading a Certificate in PEM format or requesting a managed *Let's Encrypt* Certificate. If omitted defaults to `uploaded`.


# Enum Type Name

`Type1Enum`


# Fields

| Name |
|  --- |
| `UPLOADED` |
| `MANAGED` |


# Example

```python
from hetznercloudapi.models.type_1_enum import Type1Enum

type_1 = Type1Enum.UPLOADED
```



