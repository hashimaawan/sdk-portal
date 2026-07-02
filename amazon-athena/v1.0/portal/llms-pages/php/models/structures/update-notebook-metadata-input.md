# Update Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZU5vdGVib29rTWV0YWRhdGFJbnB1dA

*This model accepts additional fields of type array.*


# Class Name

`UpdateNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `notebookId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | getNotebookId(): string | setNotebookId(string notebookId): void |
| `clientRequestToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | getClientRequestToken(): ?string | setClientRequestToken(?string clientRequestToken): void |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getName(): string | setName(string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\UpdateNotebookMetadataInputBuilder;
use AmazonAthenaLib\ApiHelper;

$updateNotebookMetadataInput = UpdateNotebookMetadataInputBuilder::init(
    'NotebookId8',
    'Name8'
)
    ->clientRequestToken('ClientRequestToken2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



