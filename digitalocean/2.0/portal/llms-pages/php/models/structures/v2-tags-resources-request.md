# V2 Tags Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNvdXJjZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2TagsResourcesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `resources` | [`Resources3[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/resources-3.md) | Required | An array of objects containing resource_id and resource_type  attributes. | getResources(): array | setResources(array resources): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2TagsResourcesRequestBuilder;
use DigitalOceanApiLib\Models\Builders\Resources3Builder;
use DigitalOceanApiLib\Models\ResourceType2;
use DigitalOceanApiLib\ApiHelper;

$v2TagsResourcesRequest = V2TagsResourcesRequestBuilder::init(
    [
        Resources3Builder::init()
            ->resourceId('9569411')
            ->resourceType(ResourceType2::DROPLET)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build(),
        Resources3Builder::init()
            ->resourceId('7555620')
            ->resourceType(ResourceType2::IMAGE)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build(),
        Resources3Builder::init()
            ->resourceId('3d80cb72-342b-4aaa-b92e-4e4abb24a933')
            ->resourceType(ResourceType2::VOLUME)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



