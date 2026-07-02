# Domains Patch Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkRvbWFpbiUyNTIwUmVjb3JkcyUyRmRvbWFpbnNfcGF0Y2hfcmVjb3Jk

To update an existing record, send a PATCH request to
`/v2/domains/$DOMAIN_NAME/records/$DOMAIN_RECORD_ID`. Any attribute valid for
the record type can be set to a new value for the record.

See the [attribute table](#tag/Domain-Records) for details regarding record
types and their respective attributes.

```php
function domainsPatchRecord(string $domainName, int $domainRecordId, ?DomainRecord $body = null): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domainName` | `string` | Template, Required | The name of the domain itself. |
| `domainRecordId` | `int` | Template, Required | The unique identifier of the domain record. |
| `body` | [`?DomainRecord`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/domain-record.md) | Body, Optional | - |


# Response Type

**200**: The response will be a JSON object with a key called `domain_record`. The value of this will be a domain record object which contains the standard domain record attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2DomainsRecordsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-domains-records-response-1.md).


# Example Usage

```php
$domainName = 'example.com';

$domainRecordId = 3352896;

$body = DomainRecordBuilder::init(
    'A'
)
    ->name('blog')
    ->build();

$domainRecordsApi = $client->getDomainRecordsApi();
$apiResponse = $domainRecordsApi->domainsPatchRecord(
    $domainName,
    $domainRecordId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2DomainsRecordsResponse1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



