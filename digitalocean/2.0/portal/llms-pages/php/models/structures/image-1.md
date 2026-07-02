# Image 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkltYWdlMQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Image1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `createdAt` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the image was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `description` | `?string` | Optional | An optional free-form text field to describe an image. | getDescription(): ?string | setDescription(?string description): void |
| `distribution` | [`?string(Distribution)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/distribution.md) | Optional | The name of a custom image's distribution. Currently, the valid values are  `Arch Linux`, `CentOS`, `CoreOS`, `Debian`, `Fedora`, `Fedora Atomic`,  `FreeBSD`, `Gentoo`, `openSUSE`, `RancherOS`, `Rocky Linux`, `Ubuntu`, and `Unknown`.  Any other value will be accepted but ignored, and `Unknown` will be used in its place. | getDistribution(): ?string | setDistribution(?string distribution): void |
| `errorMessage` | `?string` | Optional | A string containing information about errors that may occur when importing<br>a custom image. | getErrorMessage(): ?string | setErrorMessage(?string errorMessage): void |
| `id` | `?int` | Optional, Read-only | A unique number that can be used to identify and reference a specific image. | getId(): ?int | setId(?int id): void |
| `minDiskSize` | `?int` | Optional | The minimum disk size in GB required for a Droplet to use this image.<br><br>**Constraints**: `>= 0` | getMinDiskSize(): ?int | setMinDiskSize(?int minDiskSize): void |
| `name` | `?string` | Optional | The display name that has been given to an image.  This is what is shown in the control panel and is generally a descriptive title for the image in question. | getName(): ?string | setName(?string name): void |
| `public` | `?bool` | Optional | This is a boolean value that indicates whether the image in question is public or not. An image that is public is available to all accounts. A non-public image is only accessible from your account. | getPublic(): ?bool | setPublic(?bool public): void |
| `regions` | [`?(string(Region2)[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/region-2.md) | Optional | This attribute is an array of the regions that the image is available in. The regions are represented by their identifying slug values. | getRegions(): ?array | setRegions(?array regions): void |
| `sizeGigabytes` | `?float` | Optional | The size of the image in gigabytes. | getSizeGigabytes(): ?float | setSizeGigabytes(?float sizeGigabytes): void |
| `slug` | `?string` | Optional | A uniquely identifying string that is associated with each of the DigitalOcean-provided public images. These can be used to reference a public image as an alternative to the numeric id. | getSlug(): ?string | setSlug(?string slug): void |
| `status` | [`?string(Status7)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-7.md) | Optional | A status string indicating the state of a custom image. This may be `NEW`,<br>`available`, `pending`, `deleted`, or `retired`. | getStatus(): ?string | setStatus(?string status): void |
| `tags` | `?(string[])` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. | getTags(): ?array | setTags(?array tags): void |
| `type` | [`?string(Type9)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-9.md) | Optional | Describes the kind of image. It may be one of `base`, `snapshot`, `backup`, `custom`, or `admin`. Respectively, this specifies whether an image is a DigitalOcean base OS image, user-generated Droplet snapshot, automatically created Droplet backup, user-provided virtual machine image, or an image used for DigitalOcean managed resources (e.g. DOKS worker nodes). | getType(): ?string | setType(?string type): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Image1Builder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Distribution;
use DigitalOceanApiLib\Models\Region2;
use DigitalOceanApiLib\Models\Status7;
use DigitalOceanApiLib\Models\Type9;
use DigitalOceanApiLib\ApiHelper;

$image1 = Image1Builder::init()
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2020-05-04T22:23:02Z'))
    ->description('description2')
    ->distribution(Distribution::UBUNTU)
    ->errorMessage('error_message0')
    ->id(7555620)
    ->minDiskSize(20)
    ->name('Nifty New Snapshot')
    ->public(true)
    ->regions(
        [
            Region2::NYC1,
            Region2::NYC2
        ]
    )
    ->sizeGigabytes(2.34)
    ->slug('nifty1')
    ->status(Status7::NEW_)
    ->tags(
        [
            'base-image',
            'prod'
        ]
    )
    ->type(Type9::SNAPSHOT)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



