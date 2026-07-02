# Image 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkltYWdlMQ

*This model accepts additional fields of type Object.*


# Class Name

`Image1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the image was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `Description` | `String` | Optional | An optional free-form text field to describe an image. | String getDescription() | setDescription(String description) |
| `Distribution` | [`Distribution`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/distribution.md) | Optional | The name of a custom image's distribution. Currently, the valid values are  `Arch Linux`, `CentOS`, `CoreOS`, `Debian`, `Fedora`, `Fedora Atomic`,  `FreeBSD`, `Gentoo`, `openSUSE`, `RancherOS`, `Rocky Linux`, `Ubuntu`, and `Unknown`.  Any other value will be accepted but ignored, and `Unknown` will be used in its place. | Distribution getDistribution() | setDistribution(Distribution distribution) |
| `ErrorMessage` | `String` | Optional | A string containing information about errors that may occur when importing<br>a custom image. | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `Id` | `Integer` | Optional, Read-only | A unique number that can be used to identify and reference a specific image. | Integer getId() | setId(Integer id) |
| `MinDiskSize` | `Integer` | Optional | The minimum disk size in GB required for a Droplet to use this image.<br><br>**Constraints**: `>= 0` | Integer getMinDiskSize() | setMinDiskSize(Integer minDiskSize) |
| `Name` | `String` | Optional | The display name that has been given to an image.  This is what is shown in the control panel and is generally a descriptive title for the image in question. | String getName() | setName(String name) |
| `Public` | `Boolean` | Optional | This is a boolean value that indicates whether the image in question is public or not. An image that is public is available to all accounts. A non-public image is only accessible from your account. | Boolean getPublic() | setPublic(Boolean mPublic) |
| `Regions` | [`List<Region2>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/region-2.md) | Optional | This attribute is an array of the regions that the image is available in. The regions are represented by their identifying slug values. | List<Region2> getRegions() | setRegions(List<Region2> regions) |
| `SizeGigabytes` | `Double` | Optional | The size of the image in gigabytes. | Double getSizeGigabytes() | setSizeGigabytes(Double sizeGigabytes) |
| `Slug` | `String` | Optional | A uniquely identifying string that is associated with each of the DigitalOcean-provided public images. These can be used to reference a public image as an alternative to the numeric id. | String getSlug() | setSlug(String slug) |
| `Status` | [`Status7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-7.md) | Optional | A status string indicating the state of a custom image. This may be `NEW`,<br>`available`, `pending`, `deleted`, or `retired`. | Status7 getStatus() | setStatus(Status7 status) |
| `Tags` | `List<String>` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. | List<String> getTags() | setTags(List<String> tags) |
| `Type` | [`Type9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-9.md) | Optional | Describes the kind of image. It may be one of `base`, `snapshot`, `backup`, `custom`, or `admin`. Respectively, this specifies whether an image is a DigitalOcean base OS image, user-generated Droplet snapshot, automatically created Droplet backup, user-provided virtual machine image, or an image used for DigitalOcean managed resources (e.g. DOKS worker nodes). | Type9 getType() | setType(Type9 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Distribution;
import com.digitalocean.api.models.Image1;
import com.digitalocean.api.models.Region2;
import com.digitalocean.api.models.Status7;
import com.digitalocean.api.models.Type9;
import java.io.IOException;
import java.util.Arrays;

Image1 image1 = new Image1.Builder()
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2020-05-04T22:23:02Z"))
    .description("description2")
    .distribution(Distribution.UBUNTU)
    .errorMessage("error_message0")
    .id(7555620)
    .minDiskSize(20)
    .name("Nifty New Snapshot")
    .mPublic(true)
    .regions(Arrays.asList(
        Region2.NYC1,
        Region2.NYC2
    ))
    .sizeGigabytes(2.34D)
    .slug("nifty1")
    .status(Status7.NEW)
    .tags(Arrays.asList(
        "base-image",
        "prod"
    ))
    .type(Type9.SNAPSHOT)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



