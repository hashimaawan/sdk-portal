# List Named Queries Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3ROYW1lZFF1ZXJpZXNPdXRwdXQ

*This model accepts additional fields of type array.*


# Class Name

`ListNamedQueriesOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `namedQueryIds` | `?(string[])` | Optional | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getNamedQueryIds(): ?array | setNamedQueryIds(?array namedQueryIds): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListNamedQueriesOutputBuilder;
use AmazonAthenaLib\ApiHelper;

$listNamedQueriesOutput = ListNamedQueriesOutputBuilder::init()
    ->namedQueryIds(
        [
            'NamedQueryIds5',
            'NamedQueryIds4',
            'NamedQueryIds3'
        ]
    )
    ->nextToken('NextToken2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



