# V2 Kubernetes Clusters Node Pools Recycle Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlY3ljbGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsRecycleRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nodes` | `?(string[])` | Optional | - | getNodes(): ?array | setNodes(?array nodes): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersNodePoolsRecycleRequestBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2KubernetesClustersNodePoolsRecycleRequest = V2KubernetesClustersNodePoolsRecycleRequestBuilder::init()
    ->nodes(
        [
            'd8db5e1a-6103-43b5-a7b3-8a948210a9fc'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



