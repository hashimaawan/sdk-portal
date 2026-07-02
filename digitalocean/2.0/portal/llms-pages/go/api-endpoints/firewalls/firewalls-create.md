# Firewalls Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRmZpcmV3YWxsc19jcmVhdGU

To create a new firewall, send a POST request to `/v2/firewalls`. The request
must contain at least one inbound or outbound access rule.

```go
FirewallsCreate(
    ctx context.Context,
    body *models.V2FirewallsRequest) (
    models.ApiResponse[models.V2FirewallsResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`*models.V2FirewallsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-firewalls-request.md) | Body, Optional | - |


# Response Type

**202**: The response will be a JSON object with a firewall key. This will be set to an object containing the standard firewall attributes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2FirewallsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-firewalls-response-1.md).


# Example Usage

```go
ctx := context.Background()

body := models.V2FirewallsRequest{
    DropletIds:            models.NewOptional(models.ToPointer([]int{
        8043964,
    })),
    Name:                  "firewall",
    InboundRules:          []models.InboundRule{
        models.InboundRule{
            Ports:                 "80",
            Protocol:              models.Protocol_Tcp,
            Sources:               models.Sources{
                LoadBalancerUids:      []string{
                    "4de7ac8b-495b-4884-9a69-1050c6793cd6",
                },
            },
        },
        models.InboundRule{
            Ports:                 "22",
            Protocol:              models.Protocol_Tcp,
            Sources:               models.Sources{
                Addresses:             []string{
                    "18.0.0.0/8",
                },
                Tags:                  models.NewOptional(models.ToPointer([]string{
                    "gateway",
                })),
            },
        },
    },
    OutboundRules:         []models.OutboundRule{
        models.OutboundRule{
            Ports:                 "80",
            Protocol:              models.Protocol_Tcp,
            Destinations:          models.Destinations{
                Addresses:             []string{
                    "0.0.0.0/0",
                    "::/0",
                },
            },
        },
    },
}

apiResponse, err := firewallsApi.FirewallsCreate(ctx, &body)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.V21Clicks401Error:
            log.Fatalln("V21Clicks401ErrorException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Example Response *(as JSON)*

```json
{
  "firewall": {
    "created_at": "2017-05-23T21:24:00Z",
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
    "name": "firewall",
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
    "tags": []
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



