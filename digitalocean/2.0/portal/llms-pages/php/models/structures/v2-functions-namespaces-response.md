# V2 Functions Namespaces Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `namespaces` | [`?(MNamespace[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/namespace.md) | Optional | - | getNamespaces(): ?array | setNamespaces(?array namespaces): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2FunctionsNamespacesResponseBuilder;
use DigitalOceanApiLib\Models\Builders\MNamespaceBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2FunctionsNamespacesResponse = V2FunctionsNamespacesResponseBuilder::init()
    ->namespaces(
        [
            MNamespaceBuilder::init()
                ->apiHost('api_host8')
                ->createdAt('created_at0')
                ->key('key2')
                ->label('label2')
                ->namespace('namespace0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            MNamespaceBuilder::init()
                ->apiHost('api_host8')
                ->createdAt('created_at0')
                ->key('key2')
                ->label('label2')
                ->namespace('namespace0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



