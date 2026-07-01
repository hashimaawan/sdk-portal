# Update a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZVcGRhdGUlMjUyMGElMjUyMFNlcnZlcg

Updates a Server. You can update a Server’s name and a Server’s labels.
Please note that Server names must be unique per Project and valid hostnames as per RFC 1123 (i.e. may only contain letters, digits, periods, and dashes).
Also note that when updating labels, the Server’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```php
function updateAServer(int $id, ?UpdateServerRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`?UpdateServerRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/update-server-request.md) | Body, Optional | - |


# Response Type

**200**: The `server` key in the reply contains the updated Server

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ServersResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/servers-response-2.md).


# Example Usage

```php
$id = 112;

$body = UpdateServerRequestBuilder::init()
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('my-server')
    ->build();

$serversApi = $client->getServersApi();
$apiResponse = $serversApi->updateAServer(
    $id,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ServersResponse2:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



