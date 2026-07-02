# Resources 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlc291cmNlczI

An embedded object containing key value pairs of resource type and resource statistics. It also includes a count of the total number of resources tagged with the current tag as well as a `last_tagged_uri` attribute set to the last resource tagged with the current tag.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Resources2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `count` | `?int` | Optional | The number of tagged objects for this type of resource.<br><br>**Constraints**: `>= 0` | getCount(): ?int | setCount(?int count): void |
| `lastTaggedUri` | `?string` | Optional | The URI for the last tagged object for this type of resource. | getLastTaggedUri(): ?string | setLastTaggedUri(?string lastTaggedUri): void |
| `databases` | [`?Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. | getDatabases(): ?Databases | setDatabases(?Databases databases): void |
| `droplets` | [`?Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. | getDroplets(): ?Databases | setDroplets(?Databases droplets): void |
| `imgages` | [`?Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. | getImgages(): ?Databases | setImgages(?Databases imgages): void |
| `volumeSnapshots` | [`?Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. | getVolumeSnapshots(): ?Databases | setVolumeSnapshots(?Databases volumeSnapshots): void |
| `volumes` | [`?Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. | getVolumes(): ?Databases | setVolumes(?Databases volumes): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Resources2Builder;
use DigitalOceanApiLib\Models\Builders\DatabasesBuilder;
use DigitalOceanApiLib\ApiHelper;

$resources2 = Resources2Builder::init()
    ->count(5)
    ->lastTaggedUri('https://api.digitalocean.com/v2/images/7555620')
    ->databases(
        DatabasesBuilder::init()
            ->count(1)
            ->lastTaggedUri('https://api.digitalocean.com/v2/databases/b92438f6-ba03-416c-b642-e9236db91976')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->droplets(
        DatabasesBuilder::init()
            ->count(1)
            ->lastTaggedUri('https://api.digitalocean.com/v2/droplets/3164444')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->imgages(
        DatabasesBuilder::init()
            ->count(158)
            ->lastTaggedUri('last_tagged_uri4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->volumeSnapshots(
        DatabasesBuilder::init()
            ->count(1)
            ->lastTaggedUri('https://api.digitalocean.com/v2/snapshots/1f6f46e8-6b60-11e9-be4e-0a58ac144519')
            ->build()
    )
    ->volumes(
        DatabasesBuilder::init()
            ->count(1)
            ->lastTaggedUri('https://api.digitalocean.com/v2/volumes/3d80cb72-342b-4aaa-b92e-4e4abb24a933')
            ->build()
    )
    ->additionalProperty('images', ApiHelper::deserialize('{"count":1,"last_tagged_uri":"https://api.digitalocean.com/v2/images/7555620"}'))
    ->build();
```



