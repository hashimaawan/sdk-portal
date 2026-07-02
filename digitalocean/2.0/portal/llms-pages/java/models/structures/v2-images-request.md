# V2 Images Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2ImagesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | An optional free-form text field to describe an image. | String getDescription() | setDescription(String description) |
| `Distribution` | [`Distribution`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/distribution.md) | Optional | The name of a custom image's distribution. Currently, the valid values are  `Arch Linux`, `CentOS`, `CoreOS`, `Debian`, `Fedora`, `Fedora Atomic`,  `FreeBSD`, `Gentoo`, `openSUSE`, `RancherOS`, `Rocky Linux`, `Ubuntu`, and `Unknown`.  Any other value will be accepted but ignored, and `Unknown` will be used in its place. | Distribution getDistribution() | setDistribution(Distribution distribution) |
| `Name` | `String` | Required | The display name that has been given to an image.  This is what is shown in the control panel and is generally a descriptive title for the image in question. | String getName() | setName(String name) |
| `Region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. | Region2 getRegion() | setRegion(Region2 region) |
| `Tags` | `List<String>` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. | List<String> getTags() | setTags(List<String> tags) |
| `Url` | `String` | Required | A URL from which the custom Linux virtual machine image may be retrieved.  The image it points to must be in the raw, qcow2, vhdx, vdi, or vmdk format.  It may be compressed using gzip or bzip2 and must be smaller than 100 GB after being decompressed. | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Distribution;
import com.digitalocean.api.models.Region2;
import com.digitalocean.api.models.V2ImagesRequest;
import java.io.IOException;
import java.util.Arrays;

V2ImagesRequest v2ImagesRequest = new V2ImagesRequest.Builder(
    "ubuntu-18.04-minimal",
    Region2.NYC3,
    "http://cloud-images.ubuntu.com/minimal/releases/bionic/release/ubuntu-18.04-minimal-cloudimg-amd64.img"
)
.description("Cloud-optimized image w/ small footprint")
.distribution(Distribution.UBUNTU)
.tags(Arrays.asList(
        "base-image",
        "prod"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



