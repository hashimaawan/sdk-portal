# Delete Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkRlbGV0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type array.*


# Class Name

`DeleteNamedQueryInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `namedQueryId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getNamedQueryId(): string | setNamedQueryId(string namedQueryId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\DeleteNamedQueryInputBuilder;
use AmazonAthenaLib\ApiHelper;

$deleteNamedQueryInput = DeleteNamedQueryInputBuilder::init(
    'NamedQueryId4'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



