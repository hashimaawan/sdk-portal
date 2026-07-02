# V2 1 Clicks Kubernetes Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjAxJTI1MjBDbGlja3MlMjUyMEt1YmVybmV0ZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V21ClicksKubernetesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `addonSlugs` | `string[]` | Required | An array of 1-Click Application slugs to be installed to the Kubernetes cluster. | getAddonSlugs(): array | setAddonSlugs(array addonSlugs): void |
| `clusterUuid` | `string` | Required | A unique ID for the Kubernetes cluster to which the 1-Click Applications will be installed. | getClusterUuid(): string | setClusterUuid(string clusterUuid): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V21ClicksKubernetesRequestBuilder;
use DigitalOceanApiLib\ApiHelper;

$v21ClicksKubernetesRequest = V21ClicksKubernetesRequestBuilder::init(
    [
        'kube-state-metrics',
        'loki'
    ],
    '50a994b6-c303-438f-9495-7e896cfe6b08'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



