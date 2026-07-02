# Kernel

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRktlcm5lbA

**Note**: All Droplets created after March 2017 use internal kernels by default.
These Droplets will have this attribute set to `null`.

The current [kernel](https://www.digitalocean.com/docs/droplets/how-to/kernel/)
for Droplets with externally managed kernels. This will initially be set to
the kernel of the base image when the Droplet is created.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Kernel`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Optional | A unique number used to identify and reference a specific kernel. |
| `name` | `str` | Optional | The display name of the kernel. This is shown in the web UI and is generally a descriptive title for the kernel in question. |
| `version` | `str` | Optional | A standard kernel version string representing the version, patch, and release information. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.kernel import Kernel

kernel = Kernel(
    id=7515,
    name='DigitalOcean GrubLoader v0.2 (20160714)',
    version='2016.07.13-DigitalOcean_loader_Ubuntu',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



