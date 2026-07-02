# Data

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRhdGE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Data`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `result` | [`Result[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/result.md) | Required | Result of query. | getResult(): array | setResult(array result): void |
| `resultType` | `string` | Required, Constant | **Value**: `'matrix'` | getResultType(): string | setResultType(string resultType): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\DataBuilder;
use DigitalOceanApiLib\Models\Builders\ResultBuilder;
use DigitalOceanApiLib\ApiHelper;

$data = DataBuilder::init(
    [
        ResultBuilder::init(
            [
                'host_id' => '19201920'
            ],
            [
                [
                    1435781430,
                    '1'
                ],
                [
                    1435781445,
                    '1'
                ]
            ]
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



