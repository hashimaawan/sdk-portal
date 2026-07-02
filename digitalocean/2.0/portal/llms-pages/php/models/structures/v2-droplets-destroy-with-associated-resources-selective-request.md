# V2 Droplets Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing information about a resource to be scheduled for deletion.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `floatingIps` | `?(string[])` | Optional | An array of unique identifiers for the floating IPs to be scheduled for deletion. | getFloatingIps(): ?array | setFloatingIps(?array floatingIps): void |
| `reservedIps` | `?(string[])` | Optional | An array of unique identifiers for the reserved IPs to be scheduled for deletion. | getReservedIps(): ?array | setReservedIps(?array reservedIps): void |
| `snapshots` | `?(string[])` | Optional | An array of unique identifiers for the snapshots to be scheduled for deletion. | getSnapshots(): ?array | setSnapshots(?array snapshots): void |
| `volumeSnapshots` | `?(string[])` | Optional | An array of unique identifiers for the volume snapshots to be scheduled for deletion. | getVolumeSnapshots(): ?array | setVolumeSnapshots(?array volumeSnapshots): void |
| `volumes` | `?(string[])` | Optional | An array of unique identifiers for the volumes to be scheduled for deletion. | getVolumes(): ?array | setVolumes(?array volumes): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DropletsDestroyWithAssociatedResourcesSelectiveRequestBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2DropletsDestroyWithAssociatedResourcesSelectiveRequest = V2DropletsDestroyWithAssociatedResourcesSelectiveRequestBuilder::init()
    ->floatingIps(
        [
            '6186916'
        ]
    )
    ->reservedIps(
        [
            '6186916'
        ]
    )
    ->snapshots(
        [
            '61486916'
        ]
    )
    ->volumeSnapshots(
        [
            'edb0478d-7436-11ea-86e6-0a58ac144b91'
        ]
    )
    ->volumes(
        [
            'ba49449a-7435-11ea-b89e-0a58ac14480f'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



