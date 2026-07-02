# Update Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZU5vdGVib29rSW5wdXQ

*This model accepts additional fields of type array.*


# Class Name

`UpdateNotebookInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `notebookId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | getNotebookId(): string | setNotebookId(string notebookId): void |
| `payload` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` | getPayload(): string | setPayload(string payload): void |
| `type` | [`string(NotebookType2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/notebook-type-2.md) | Required | - | getType(): string | setType(string type): void |
| `sessionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): ?string | setSessionId(?string sessionId): void |
| `clientRequestToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | getClientRequestToken(): ?string | setClientRequestToken(?string clientRequestToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\UpdateNotebookInputBuilder;
use AmazonAthenaLib\Models\NotebookType2;
use AmazonAthenaLib\ApiHelper;

$updateNotebookInput = UpdateNotebookInputBuilder::init(
    'NotebookId8',
    'Payload4',
    NotebookType2::IPYNB
)
    ->sessionId('SessionId0')
    ->clientRequestToken('ClientRequestToken2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



