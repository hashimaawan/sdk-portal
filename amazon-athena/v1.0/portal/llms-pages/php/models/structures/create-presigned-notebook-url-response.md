# Create Presigned Notebook Url Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`CreatePresignedNotebookUrlResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `notebookUrl` | `string` | Required | - | getNotebookUrl(): string | setNotebookUrl(string notebookUrl): void |
| `authToken` | `string` | Required | **Constraints**: *Maximum Length*: `2048` | getAuthToken(): string | setAuthToken(string authToken): void |
| `authTokenExpirationTime` | `int` | Required | - | getAuthTokenExpirationTime(): int | setAuthTokenExpirationTime(int authTokenExpirationTime): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CreatePresignedNotebookUrlResponseBuilder;
use AmazonAthenaLib\ApiHelper;

$createPresignedNotebookUrlResponse = CreatePresignedNotebookUrlResponseBuilder::init(
    'NotebookUrl0',
    'AuthToken4',
    240
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



