# Firewalls Update

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRmZpcmV3YWxsc191cGRhdGU

To update the configuration of an existing firewall, send a PUT request to
`/v2/firewalls/$FIREWALL_ID`. The request should contain a full representation
of the firewall including existing attributes. **Note that any attributes that
are not provided will be reset to their default values.**

```php
function firewallsUpdate(string $firewallId, ?V2FirewallsRequest $body = null): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewallId` | `string` | Template, Required | A unique ID that can be used to identify and reference a firewall. |
| `body` | [`?V2FirewallsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-firewalls-request.md) | Body, Optional | - |


# Response Type

**200**: The response will be a JSON object with a `firewall` key. This will be set to an object containing the standard firewall attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2FirewallsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-firewalls-response-1.md).


# Example Usage

```php
$firewallId = 'bb4b2611-3d72-467b-8602-280330ecd65c';

$body = V2FirewallsRequestBuilder::init(
    'frontend-firewall'
)
    ->dropletIds(
        [
            8043964
        ]
    )
    ->tags(
        [
            'frontend'
        ]
    )
    ->inboundRules(
        [
            InboundRuleBuilder::init(
                '8080',
                Protocol::TCP,
                SourcesBuilder::init()
                    ->loadBalancerUids(
                        [
                            '4de7ac8b-495b-4884-9a69-1050c6793cd6'
                        ]
                    )
                    ->build()
            )->build(),
            InboundRuleBuilder::init(
                '22',
                Protocol::TCP,
                SourcesBuilder::init()
                    ->addresses(
                        [
                            '18.0.0.0/8'
                        ]
                    )
                    ->tags(
                        [
                            'gateway'
                        ]
                    )
                    ->build()
            )->build()
        ]
    )
    ->outboundRules(
        [
            OutboundRuleBuilder::init(
                '8080',
                Protocol::TCP,
                DestinationsBuilder::init()
                    ->addresses(
                        [
                            '0.0.0.0/0',
                            '::/0'
                        ]
                    )
                    ->build()
            )->build()
        ]
    )->build();

$firewallsApi = $client->getFirewallsApi();
$apiResponse = $firewallsApi->firewallsUpdate(
    $firewallId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2FirewallsResponse1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "firewall": {
    "created_at": "2020-05-23T21:24:00Z",
    "droplet_ids": [
      8043964
    ],
    "id": "bb4b2611-3d72-467b-8602-280330ecd65c",
    "inbound_rules": [
      {
        "ports": "80",
        "protocol": "tcp",
        "sources": {
          "load_balancer_uids": [
            "4de7ac8b-495b-4884-9a69-1050c6793cd6"
          ]
        }
      },
      {
        "ports": "22",
        "protocol": "tcp",
        "sources": {
          "addresses": [
            "18.0.0.0/8"
          ],
          "tags": [
            "gateway"
          ]
        }
      }
    ],
    "name": "frontend-firewall",
    "outbound_rules": [
      {
        "destinations": {
          "addresses": [
            "0.0.0.0/0",
            "::/0"
          ]
        },
        "ports": "80",
        "protocol": "tcp"
      }
    ],
    "pending_changes": [
      {
        "droplet_id": 8043964,
        "removing": false,
        "status": "waiting"
      }
    ],
    "status": "waiting",
    "tags": [
      "frontend"
    ]
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



