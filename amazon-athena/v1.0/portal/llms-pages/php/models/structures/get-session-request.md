# Get Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFNlc3Npb25SZXF1ZXN0


# Class Name

`GetSessionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): string | setSessionId(string sessionId): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetSessionRequestBuilder;

$getSessionRequest = GetSessionRequestBuilder::init(
    'SessionId2'
)->build();
```



