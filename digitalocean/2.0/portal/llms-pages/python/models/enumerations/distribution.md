# Distribution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkRpc3RyaWJ1dGlvbg

The name of a custom image's distribution. Currently, the valid values are  `Arch Linux`, `CentOS`, `CoreOS`, `Debian`, `Fedora`, `Fedora Atomic`,  `FreeBSD`, `Gentoo`, `openSUSE`, `RancherOS`, `Rocky Linux`, `Ubuntu`, and `Unknown`.  Any other value will be accepted but ignored, and `Unknown` will be used in its place.


# Enum Type Name

`Distribution`


# Fields

| Name |
|  --- |
| `ENUM_ARCH_LINUX` |
| `CENTOS` |
| `COREOS` |
| `DEBIAN` |
| `FEDORA` |
| `ENUM_FEDORA_ATOMIC` |
| `FREEBSD` |
| `GENTOO` |
| `OPENSUSE` |
| `RANCHEROS` |
| `ENUM_ROCKY_LINUX` |
| `UBUNTU` |
| `UNKNOWN` |


# Example

```python
from digitaloceanapi.models.distribution import Distribution

distribution = Distribution.ENUM_FEDORA_ATOMIC
```



