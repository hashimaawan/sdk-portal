# Default Toast Compression

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkRlZmF1bHRUb2FzdENvbXByZXNzaW9u

Specifies the default TOAST compression method for values of compressible columns (the default is lz4).


# Enum Type Name

`DefaultToastCompression`


# Fields

| Name |
|  --- |
| `LZ4` |
| `PGLZ` |


# Example

```python
from digitaloceanapi.models.default_toast_compression import DefaultToastCompression

default_toast_compression = DefaultToastCompression.LZ4
```



