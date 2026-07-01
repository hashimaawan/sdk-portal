# Update a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGVXBkYXRlJTI1MjBhJTI1MjBOZXR3b3Jr

Updates the network properties.

Note that when updating labels, the network’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

Note: if the network object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```go
UpdateANetwork(
    ctx context.Context,
    id int,
    body *models.UpdateNetworkRequest) (
    models.ApiResponse[models.NetworksResponse1],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the network |
| `body` | [`*models.UpdateNetworkRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/update-network-request.md) | Body, Optional | - |


# Response Type

**200**: The `network` key contains the updated network

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.NetworksResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/networks-response-1.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.UpdateNetworkRequest{
    Name:                 models.ToPointer("new-name"),
}

apiResponse, err := networksController.UpdateANetwork(ctx, id, &body)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Example Response *(as JSON)*

```json
{
  "network": {
    "created": "2016-01-30T23:50:00+00:00",
    "id": 4711,
    "ip_range": "10.0.0.0/16",
    "labels": {
      "labelkey": "value"
    },
    "load_balancers": [
      42
    ],
    "name": "new-name",
    "protection": {
      "delete": false
    },
    "routes": [
      {
        "destination": "10.100.1.0/24",
        "gateway": "10.0.1.1"
      }
    ],
    "servers": [
      42
    ],
    "subnets": [
      {
        "gateway": "10.0.0.1",
        "ip_range": "10.0.1.0/24",
        "network_zone": "eu-central",
        "type": "cloud"
      }
    ]
  }
}
```



