# Delete a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGRGVsZXRlJTI1MjBhJTI1MjBOZXR3b3Jr

Deletes a network. If there are Servers attached they will be detached in the background.

Note: if the network object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```php
function deleteANetwork(int $id): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the network |


# Response Type

**204**: Network deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$id = 112;

$networksApi = $client->getNetworksApi();
$apiResponse = $networksApi->deleteANetwork($id);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'void:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



