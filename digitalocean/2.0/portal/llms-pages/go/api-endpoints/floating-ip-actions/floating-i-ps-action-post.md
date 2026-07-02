# Floating I Ps Action Post

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUCUyNTIwQWN0aW9ucyUyRmZsb2F0aW5nSVBzQWN0aW9uX3Bvc3Q

To initiate an action on a floating IP send a POST request to
`/v2/floating_ips/$FLOATING_IP/actions`. In the JSON body to the request,
set the `type` attribute to on of the supported action types:

| Action     | Details
|------------|--------
| `assign`   | Assigns a floating IP to a Droplet
| `unassign` | Unassign a floating IP from a Droplet

```go
FloatingIPsActionPost(
    ctx context.Context,
    floatingIp string,
    body *models.FloatingIPsActionPostBody) (
    models.ApiResponse[models.V2FloatingIpsActionsResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floatingIp` | `string` | Template, Required | A floating IP address. |
| `body` | [`*models.FloatingIPsActionPostBody`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/oneof-anyof-definitions/floating-i-ps-action-post-body.md) | Body, Optional | This is a container for any-of cases. |


# Response Type

**201**: The response will be an object with a key called `action`. The value of this will be an object that contains the standard floating IP action attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2FloatingIpsActionsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-floating-ips-actions-response-1.md).


# Example Usage

```go
ctx := context.Background()

floatingIp := "45.55.96.47"

body := models.FloatingIPsActionPostBodyContainer.FromBaseType(models.BaseTypeInterface(&models.V2ReservedIpsActionsRequestInterface(&models.V2ReservedIpsActionsRequest{
    BaseType:  models.BaseType{
        Type:                  models.ToPointer("V2 Reserved Ips Actions Request"),
    },
    DropletId: 758604968,
})))

apiResponse, err := floatingIpActionsApi.FloatingIPsActionPost(ctx, floatingIp, &body)
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


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



