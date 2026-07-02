# Type 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlR5cGU5

Describes the kind of image. It may be one of `base`, `snapshot`, `backup`, `custom`, or `admin`. Respectively, this specifies whether an image is a DigitalOcean base OS image, user-generated Droplet snapshot, automatically created Droplet backup, user-provided virtual machine image, or an image used for DigitalOcean managed resources (e.g. DOKS worker nodes).


# Enum Type Name

`Type9`


# Fields

| Name |
|  --- |
| `BASE` |
| `SNAPSHOT` |
| `BACKUP` |
| `CUSTOM` |
| `ADMIN` |


# Example

```python
from digitaloceanapi.models.type_9 import Type9

type_9 = Type9.SNAPSHOT
```



