# Update a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZVcGRhdGUlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Updates the description or labels of a Floating IP.
Also note that when updating labels, the Floating IP’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```go
UpdateAFloatingIP(
    ctx context.Context,
    id int,
    body *models.UpdateFloatingIPRequest) (
    models.ApiResponse[models.FloatingIpsResponse2],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |
| `body` | [`*models.UpdateFloatingIPRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/update-floating-ip-request.md) | Body, Optional | - |


# Response Type

**200**: The `floating_ip` key in the reply contains the modified Floating IP object with the new description

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.FloatingIpsResponse2](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/floating-ips-response-2.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.UpdateFloatingIPRequest{
    Description:          models.ToPointer("Web Frontend"),
    Labels:               models.ToPointer(interface{}("[labelkey, value]")),
    Name:                 models.ToPointer("Web Frontend"),
}

apiResponse, err := floatingIPsController.UpdateAFloatingIP(ctx, id, &body)
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



