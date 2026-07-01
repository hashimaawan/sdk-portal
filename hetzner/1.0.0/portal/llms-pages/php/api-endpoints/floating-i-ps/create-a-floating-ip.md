# Create a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZDcmVhdGUlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Creates a new Floating IP assigned to a Server. If you want to create a Floating IP that is not bound to a Server, you need to provide the `home_location` key instead of `server`. This can be either the ID or the name of the Location this IP shall be created in. Note that a Floating IP can be assigned to a Server in any Location later on. For optimal routing it is advised to use the Floating IP in the same Location it was created in.

:information_source: **Note** This endpoint does not require authentication.

```php
function createAFloatingIp(?CreateFloatingIpRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`?CreateFloatingIpRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/create-floating-ip-request.md) | Body, Optional | The `type` argument is required while `home_location` and `server` are mutually exclusive. |


# Response Type

**201**: The `floating_ip` key in the reply contains the object that was just created

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`FloatingIpsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/floating-ips-response-1.md).


# Example Usage

```php
$body = CreateFloatingIpRequestBuilder::init(
    Type17::IPV4
)
    ->description('Web Frontend')
    ->homeLocation('fsn1')
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('Web Frontend')
    ->server(42)
    ->build();

$floatingIPsApi = $client->getFloatingIPsApi();
$apiResponse = $floatingIPsApi->createAFloatingIp($body);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'FloatingIpsResponse1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "create_floating_ip",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 42,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  },
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
      "env": "dev"
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



