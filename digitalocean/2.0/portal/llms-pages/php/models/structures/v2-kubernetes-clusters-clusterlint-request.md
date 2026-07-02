# V2 Kubernetes Clusters Clusterlint Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersClusterlintRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `excludeChecks` | `?(string[])` | Optional | An array of checks that will be run when clusterlint executes checks. | getExcludeChecks(): ?array | setExcludeChecks(?array excludeChecks): void |
| `excludeGroups` | `?(string[])` | Optional | An array of check groups that will be omitted when clusterlint executes checks. | getExcludeGroups(): ?array | setExcludeGroups(?array excludeGroups): void |
| `includeChecks` | `?(string[])` | Optional | An array of checks that will be run when clusterlint executes checks. | getIncludeChecks(): ?array | setIncludeChecks(?array includeChecks): void |
| `includeGroups` | `?(string[])` | Optional | An array of check groups that will be run when clusterlint executes checks. | getIncludeGroups(): ?array | setIncludeGroups(?array includeGroups): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersClusterlintRequestBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2KubernetesClustersClusterlintRequest = V2KubernetesClustersClusterlintRequestBuilder::init()
    ->excludeChecks(
        [
            'default-namespace'
        ]
    )
    ->excludeGroups(
        [
            'workload-health'
        ]
    )
    ->includeChecks(
        [
            'bare-pods',
            'resource-requirements'
        ]
    )
    ->includeGroups(
        [
            'basic',
            'doks',
            'security'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



