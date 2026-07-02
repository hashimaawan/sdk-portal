# V2 Images Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2ImagesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | An optional free-form text field to describe an image. | getDescription(): ?string | setDescription(?string description): void |
| `distribution` | [`?string(Distribution)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/distribution.md) | Optional | The name of a custom image's distribution. Currently, the valid values are  `Arch Linux`, `CentOS`, `CoreOS`, `Debian`, `Fedora`, `Fedora Atomic`,  `FreeBSD`, `Gentoo`, `openSUSE`, `RancherOS`, `Rocky Linux`, `Ubuntu`, and `Unknown`.  Any other value will be accepted but ignored, and `Unknown` will be used in its place. | getDistribution(): ?string | setDistribution(?string distribution): void |
| `name` | `string` | Required | The display name that has been given to an image.  This is what is shown in the control panel and is generally a descriptive title for the image in question. | getName(): string | setName(string name): void |
| `region` | [`string(Region2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. | getRegion(): string | setRegion(string region): void |
| `tags` | `?(string[])` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. | getTags(): ?array | setTags(?array tags): void |
| `url` | `string` | Required | A URL from which the custom Linux virtual machine image may be retrieved.  The image it points to must be in the raw, qcow2, vhdx, vdi, or vmdk format.  It may be compressed using gzip or bzip2 and must be smaller than 100 GB after being decompressed. | getUrl(): string | setUrl(string url): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2ImagesRequestBuilder;
use DigitalOceanApiLib\Models\Region2;
use DigitalOceanApiLib\Models\Distribution;
use DigitalOceanApiLib\ApiHelper;

$v2ImagesRequest = V2ImagesRequestBuilder::init(
    'ubuntu-18.04-minimal',
    Region2::NYC3,
    'http://cloud-images.ubuntu.com/minimal/releases/bionic/release/ubuntu-18.04-minimal-cloudimg-amd64.img'
)
    ->description('Cloud-optimized image w/ small footprint')
    ->distribution(Distribution::UBUNTU)
    ->tags(
        [
            'base-image',
            'prod'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



