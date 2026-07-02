# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA

*This model accepts additional fields of type array.*


# Class Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `resourceArn` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` | getResourceArn(): string | setResourceArn(string resourceArn): void |
| `tagKeys` | `string[]` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getTagKeys(): array | setTagKeys(array tagKeys): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\UntagResourceInputBuilder;
use AmazonAthenaLib\ApiHelper;

$untagResourceInput = UntagResourceInputBuilder::init(
    'ResourceARN6',
    [
        'TagKeys1',
        'TagKeys2',
        'TagKeys3'
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



