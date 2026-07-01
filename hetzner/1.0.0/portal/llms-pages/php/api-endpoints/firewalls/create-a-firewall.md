# Create a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkNyZWF0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Creates a new Firewall.

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `server_already_added`        | Server added more than one time to resource                   |
| `incompatible_network_type`   | The Network type is incompatible for the given resource       |
| `firewall_resource_not_found` | The resource the Firewall should be attached to was not found |

:information_source: **Note** This endpoint does not require authentication.

```php
function createAFirewall(?CreateFirewallRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`?CreateFirewallRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/create-firewall-request.md) | Body, Optional | - |


# Response Type

**201**: The `firewall` key contains the Firewall that was just created

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`CreateFirewallResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/create-firewall-response.md).


# Example Usage

```php
$body = CreateFirewallRequestBuilder::init(
    'Corporate Intranet Protection'
)
    ->applyTo(
        [
            ApplyToBuilder::init(
                Type7::SERVER
            )
                ->server(
                    Server2Builder::init(
                        42
                    )->build()
                )->build()
        ]
    )
    ->labels(ApiHelper::deserialize('{"env":"dev"}'))
    ->rules(
        [
            RuleBuilder::init(
                Direction::IN,
                Protocol::TCP
            )
                ->description('Allow port 80')
                ->port('80')
                ->sourceIps(
                    [
                        '28.239.13.1/32',
                        '28.239.14.0/24',
                        'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
                    ]
                )
                ->build()
        ]
    )
    ->build();

$firewallsApi = $client->getFirewallsApi();
$apiResponse = $firewallsApi->createAFirewall($body);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'CreateFirewallResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



