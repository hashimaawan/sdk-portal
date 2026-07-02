# Create Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlPdXRwdXQ

*This model accepts additional fields of type array.*


# Class Name

`CreateNamedQueryOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `namedQueryId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getNamedQueryId(): ?string | setNamedQueryId(?string namedQueryId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CreateNamedQueryOutputBuilder;
use AmazonAthenaLib\ApiHelper;

$createNamedQueryOutput = CreateNamedQueryOutputBuilder::init()
    ->namedQueryId('NamedQueryId0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



