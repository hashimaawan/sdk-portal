# Create Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZURhdGFDYXRhbG9nSW5wdXQ

*This model accepts additional fields of type array.*


# Class Name

`CreateDataCatalogInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getName(): string | setName(string name): void |
| `type` | [`string(DataCatalogType1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/data-catalog-type-1.md) | Required | - | getType(): string | setType(string type): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `parameters` | [`?Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/parameters.md) | Optional | - | getParameters(): ?Parameters | setParameters(?Parameters parameters): void |
| `tags` | [`?(Tag[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/tag.md) | Optional | - | getTags(): ?array | setTags(?array tags): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CreateDataCatalogInputBuilder;
use AmazonAthenaLib\Models\DataCatalogType1;
use AmazonAthenaLib\Models\Builders\ParametersBuilder;
use AmazonAthenaLib\Models\Builders\TagBuilder;
use AmazonAthenaLib\ApiHelper;

$createDataCatalogInput = CreateDataCatalogInputBuilder::init(
    'Name6',
    DataCatalogType1::GLUE
)
    ->description('Description2')
    ->parameters(
        ParametersBuilder::init()
            ->additionalProperty('exampleAdditionalProperty', 'Parameters_additionalProperties2')
            ->build()
    )
    ->tags(
        [
            TagBuilder::init()
                ->key('Key0')
                ->value('Value6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            TagBuilder::init()
                ->key('Key0')
                ->value('Value6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            TagBuilder::init()
                ->key('Key0')
                ->value('Value6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



