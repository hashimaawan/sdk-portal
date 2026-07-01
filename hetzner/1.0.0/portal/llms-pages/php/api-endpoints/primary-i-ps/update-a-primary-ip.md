# Update a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRlVwZGF0ZSUyNTIwYSUyNTIwUHJpbWFyeSUyNTIwSVA

Updates the Primary IP.

Note that when updating labels, the Primary IP's current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

If the Primary IP object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```php
function updateAPrimaryIp(int $id, ?UpdatePrimaryIpRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |
| `body` | [`?UpdatePrimaryIpRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/update-primary-ip-request.md) | Body, Optional | - |


# Response Type

**200**: The `primary_ip` key contains the Primary IP that was just updated

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PrimaryIpResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/primary-ip-response.md).


# Example Usage

```php
$id = 112;

$body = UpdatePrimaryIpRequestBuilder::init()
    ->autoDelete(true)
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('my-ip')
    ->build();

$primaryIPsApi = $client->getPrimaryIPsApi();
$apiResponse = $primaryIPsApi->updateAPrimaryIp(
    $id,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PrimaryIpResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



