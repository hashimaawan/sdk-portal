# Reserved I Ps Actions Post

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRlJlc2VydmVkJTI1MjBJUCUyNTIwQWN0aW9ucyUyRnJlc2VydmVkSVBzQWN0aW9uc19wb3N0

To initiate an action on a reserved IP send a POST request to
`/v2/reserved_ips/$RESERVED_IP/actions`. In the JSON body to the request,
set the `type` attribute to on of the supported action types:

| Action     | Details
|------------|--------
| `assign`   | Assigns a reserved IP to a Droplet
| `unassign` | Unassign a reserved IP from a Droplet

```php
function reservedIPsActionsPost(string $reservedIp, $body = null): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reservedIp` | `string` | Template, Required | A reserved IP address. |
| `body` | [BaseType](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/base-type.md)\|[V2ReservedIpsActionsRequest](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-reserved-ips-actions-request.md)\|null | Body, Optional | This is a container for any-of cases. |


# Response Type

**201**: The response will be an object with a key called `action`. The value of this will be an object that contains the standard reserved IP action attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2ReservedIpsActionsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-reserved-ips-actions-response-1.md).


# Example Usage

```php
$reservedIp = '45.55.96.47';

$body = V2ReservedIpsActionsRequestBuilder::init(
    758604968
)
    ->type('V2 Reserved Ips Actions Request')
    ->build();

$reservedIpActionsApi = $client->getReservedIpActionsApi();
$apiResponse = $reservedIpActionsApi->reservedIPsActionsPost(
    $reservedIp,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2ReservedIpsActionsResponse1:';
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



