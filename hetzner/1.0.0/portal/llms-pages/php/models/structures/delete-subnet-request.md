# Delete Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkRlbGV0ZVN1Ym5ldFJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`DeleteSubnetRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ipRange` | `string` | Required | IP range of subnet to delete | getIpRange(): string | setIpRange(string ipRange): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\DeleteSubnetRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$deleteSubnetRequest = DeleteSubnetRequestBuilder::init(
    '10.0.1.0/24'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



