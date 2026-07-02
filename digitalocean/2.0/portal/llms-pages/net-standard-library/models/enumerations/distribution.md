# Distribution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRpc3RyaWJ1dGlvbg

The name of a custom image's distribution. Currently, the valid values are  `Arch Linux`, `CentOS`, `CoreOS`, `Debian`, `Fedora`, `Fedora Atomic`,  `FreeBSD`, `Gentoo`, `openSUSE`, `RancherOS`, `Rocky Linux`, `Ubuntu`, and `Unknown`.  Any other value will be accepted but ignored, and `Unknown` will be used in its place.


# Enum Type Name

`Distribution`


# Fields

| Name |
|  --- |
| `EnumArchLinux` |
| `CentOs` |
| `CoreOs` |
| `Debian` |
| `Fedora` |
| `EnumFedoraAtomic` |
| `FreeBsd` |
| `Gentoo` |
| `OpenSuse` |
| `RancherOs` |
| `EnumRockyLinux` |
| `Ubuntu` |
| `Unknown` |


# Example

```csharp
using DigitalOceanApi.Standard.Models;

Distribution distribution = Distribution.EnumFedoraAtomic;
```



