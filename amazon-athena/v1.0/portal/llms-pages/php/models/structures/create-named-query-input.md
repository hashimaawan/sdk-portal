# Create Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type array.*


# Class Name

`CreateNamedQueryInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getName(): string | setName(string name): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `database` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getDatabase(): string | setDatabase(string database): void |
| `queryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | getQueryString(): string | setQueryString(string queryString): void |
| `clientRequestToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` | getClientRequestToken(): ?string | setClientRequestToken(?string clientRequestToken): void |
| `workGroup` | `?string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): ?string | setWorkGroup(?string workGroup): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CreateNamedQueryInputBuilder;
use AmazonAthenaLib\ApiHelper;

$createNamedQueryInput = CreateNamedQueryInputBuilder::init(
    'Name4',
    'Database4',
    'QueryString8'
)
    ->description('Description0')
    ->clientRequestToken('ClientRequestToken0')
    ->workGroup('WorkGroup8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



