# Image 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkltYWdlMQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Image1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional | A time value given in ISO8601 combined date and time format that represents when the image was created. |
| `description` | `str` | Optional | An optional free-form text field to describe an image. |
| `distribution` | [`Distribution`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/distribution.md) | Optional | The name of a custom image's distribution. Currently, the valid values are  `Arch Linux`, `CentOS`, `CoreOS`, `Debian`, `Fedora`, `Fedora Atomic`,  `FreeBSD`, `Gentoo`, `openSUSE`, `RancherOS`, `Rocky Linux`, `Ubuntu`, and `Unknown`.  Any other value will be accepted but ignored, and `Unknown` will be used in its place. |
| `error_message` | `str` | Optional | A string containing information about errors that may occur when importing<br>a custom image. |
| `id` | `int` | Optional, Read-only | A unique number that can be used to identify and reference a specific image. |
| `min_disk_size` | `int` | Optional | The minimum disk size in GB required for a Droplet to use this image.<br><br>**Constraints**: `>= 0` |
| `name` | `str` | Optional | The display name that has been given to an image.  This is what is shown in the control panel and is generally a descriptive title for the image in question. |
| `public` | `bool` | Optional | This is a boolean value that indicates whether the image in question is public or not. An image that is public is available to all accounts. A non-public image is only accessible from your account. |
| `regions` | [`List[Region2]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/region-2.md) | Optional | This attribute is an array of the regions that the image is available in. The regions are represented by their identifying slug values. |
| `size_gigabytes` | `float` | Optional | The size of the image in gigabytes. |
| `slug` | `str` | Optional | A uniquely identifying string that is associated with each of the DigitalOcean-provided public images. These can be used to reference a public image as an alternative to the numeric id. |
| `status` | [`Status7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status-7.md) | Optional | A status string indicating the state of a custom image. This may be `NEW`,<br>`available`, `pending`, `deleted`, or `retired`. |
| `tags` | `List[str]` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `mtype` | [`Type9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-9.md) | Optional | Describes the kind of image. It may be one of `base`, `snapshot`, `backup`, `custom`, or `admin`. Respectively, this specifies whether an image is a DigitalOcean base OS image, user-generated Droplet snapshot, automatically created Droplet backup, user-provided virtual machine image, or an image used for DigitalOcean managed resources (e.g. DOKS worker nodes). |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.distribution import Distribution
from digitaloceanapi.models.image_1 import Image1
from digitaloceanapi.models.region_2 import Region2
from digitaloceanapi.models.status_7 import Status7
from digitaloceanapi.models.type_9 import Type9

image_1 = Image1(
    created_at=dateutil.parser.parse('2020-05-04T22:23:02Z'),
    description='description0',
    distribution=Distribution.UBUNTU,
    error_message='error_message2',
    id=7555620,
    min_disk_size=20,
    name='Nifty New Snapshot',
    public=True,
    regions=[
        Region2.NYC1,
        Region2.NYC2
    ],
    size_gigabytes=2.34,
    slug='nifty1',
    status=Status7.NEW,
    tags=[
        'base-image',
        'prod'
    ],
    mtype=Type9.SNAPSHOT,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



