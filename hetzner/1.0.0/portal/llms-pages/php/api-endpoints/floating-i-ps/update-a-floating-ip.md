# Update a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZVcGRhdGUlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Updates the description or labels of a Floating IP.
Also note that when updating labels, the Floating IP’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```php
function updateAFloatingIp(int $id, ?UpdateFloatingIpRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |
| `body` | [`?UpdateFloatingIpRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/update-floating-ip-request.md) | Body, Optional | - |


# Response Type

**200**: The `floating_ip` key in the reply contains the modified Floating IP object with the new description

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`FloatingIpsResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/floating-ips-response-2.md).


# Example Usage

```php
$id = 112;

$body = UpdateFloatingIpRequestBuilder::init()
    ->description('Web Frontend')
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('Web Frontend')
    ->build();

$floatingIPsApi = $client->getFloatingIPsApi();
$apiResponse = $floatingIPsApi->updateAFloatingIp(
    $id,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'FloatingIpsResponse2:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "floating_ip": {
    "blocked": false,
    "created": "2016-01-30T23:50:00+00:00",
    "description": "Web Frontend",
    "dns_ptr": [
      {
        "dns_ptr": "server.example.com",
        "ip": "2001:db8::1"
      }
    ],
    "home_location": {
      "city": "Falkenstein",
      "country": "DE",
      "description": "Falkenstein DC Park 1",
      "id": 1,
      "latitude": 50.47612,
      "longitude": 12.370071,
      "name": "fsn1",
      "network_zone": "eu-central"
    },
    "id": 4711,
    "ip": "131.232.99.1",
    "labels": {
      "labelkey": "value"
    },
    "name": "Web Frontend",
    "protection": {
      "delete": false
    },
    "server": 42,
    "type": "ipv4"
  }
}
```



