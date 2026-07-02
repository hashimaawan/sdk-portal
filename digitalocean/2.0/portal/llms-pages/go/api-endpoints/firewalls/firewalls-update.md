# Firewalls Update

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRmZpcmV3YWxsc191cGRhdGU

To update the configuration of an existing firewall, send a PUT request to
`/v2/firewalls/$FIREWALL_ID`. The request should contain a full representation
of the firewall including existing attributes. **Note that any attributes that
are not provided will be reset to their default values.**

```go
FirewallsUpdate(
    ctx context.Context,
    firewallId uuid.UUID,
    body *models.V2FirewallsRequest) (
    models.ApiResponse[models.V2FirewallsResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewallId` | `uuid.UUID` | Template, Required | A unique ID that can be used to identify and reference a firewall. |
| `body` | [`*models.V2FirewallsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-firewalls-request.md) | Body, Optional | - |


# Response Type

**200**: The response will be a JSON object with a `firewall` key. This will be set to an object containing the standard firewall attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2FirewallsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-firewalls-response-1.md).


# Example Usage

```go
ctx := context.Background()

firewallId := uuid.MustParse("bb4b2611-3d72-467b-8602-280330ecd65c")

body := models.V2FirewallsRequest{
    DropletIds:            models.NewOptional(models.ToPointer([]int{
        8043964,
    })),
    Name:                  "frontend-firewall",
    Tags:                  models.NewOptional(models.ToPointer([]string{
        "frontend",
    })),
    InboundRules:          []models.InboundRule{
        models.InboundRule{
            Ports:                 "8080",
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
            Ports:                 "8080",
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

apiResponse, err := firewallsApi.FirewallsUpdate(ctx, firewallId, &body)
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
| 400 | Bad Request | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



