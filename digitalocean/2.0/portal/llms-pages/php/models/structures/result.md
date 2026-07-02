# Result

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Result`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `metric` | `array<string,string>` | Required | An object containing the metric labels. | getMetric(): array | setMetric(array metric): void |
| `values` | array<array<int\|string>> | Required | This is 2d Array of a container for one-of cases. | getValues(): array | setValues(array values): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ResultBuilder;
use DigitalOceanApiLib\ApiHelper;

$result = ResultBuilder::init(
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
    ->build();
```



