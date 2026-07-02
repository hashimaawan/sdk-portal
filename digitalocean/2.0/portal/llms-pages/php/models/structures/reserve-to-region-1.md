# Reserve to Region 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlc2VydmUlMjUyMHRvJTI1MjBSZWdpb24x

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`ReserveToRegion1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `projectId` | `?string` | Optional | The UUID of the project to which the reserved IP will be assigned. | getProjectId(): ?string | setProjectId(?string projectId): void |
| `region` | `string` | Required | The slug identifier for the region the reserved IP will be reserved to. | getRegion(): string | setRegion(string region): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ReserveToRegion1Builder;
use DigitalOceanApiLib\ApiHelper;

$reserveToRegion1 = ReserveToRegion1Builder::init(
    'nyc3'
)
    ->projectId('746c6152-2fa2-11ed-92d3-27aaa54e4988')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



