# V2 Kubernetes Registry Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBSZWdpc3RyeSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesRegistryRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `clusterUuids` | `?(string[])` | Optional | An array containing the UUIDs of Kubernetes clusters. | getClusterUuids(): ?array | setClusterUuids(?array clusterUuids): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesRegistryRequestBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2KubernetesRegistryRequest = V2KubernetesRegistryRequestBuilder::init()
    ->clusterUuids(
        [
            'bd5f5959-5e1e-4205-a714-a914373942af',
            '50c2f44c-011d-493e-aee5-361a4a0d1844'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



