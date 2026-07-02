# Droplets Destroy with Associated Resources Selective

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkRyb3BsZXRzJTJGZHJvcGxldHNfZGVzdHJveV93aXRoQXNzb2NpYXRlZFJlc291cmNlc1NlbGVjdGl2ZQ

To destroy a Droplet along with a sub-set of its associated resources, send a
DELETE request to the `/v2/droplets/$DROPLET_ID/destroy_with_associated_resources/selective`
endpoint. The JSON body of the request should include `reserved_ips`, `snapshots`, `volumes`,
or `volume_snapshots` keys each set to an array of IDs for the associated
resources to be destroyed. The IDs can be found by querying the Droplet's
associated resources. Any associated resource not included in the request
will remain and continue to accrue changes on your account.

A successful response will include a 202 response code and no content. Use
the status endpoint to check on the success or failure of the destruction of
the individual resources.

```go
DropletsDestroyWithAssociatedResourcesSelective(
    ctx context.Context,
    dropletId int,
    body *models.V2DropletsDestroyWithAssociatedResourcesSelectiveRequest) (
    http.Response,
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletId` | `int` | Template, Required | A unique identifier for a Droplet instance.<br><br>**Constraints**: `>= 1` |
| `body` | [`*models.V2DropletsDestroyWithAssociatedResourcesSelectiveRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-droplets-destroy-with-associated-resources-selective-request.md) | Body, Optional | - |


# Response Type

**202**: The does not indicate the success or failure of any operation, just that the request has been accepted for processing.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

dropletId := 3164444

body := models.V2DropletsDestroyWithAssociatedResourcesSelectiveRequest{
    FloatingIps:           []string{
        "6186916",
    },
    ReservedIps:           []string{
        "6186916",
    },
    Snapshots:             []string{
        "61486916",
    },
    VolumeSnapshots:       []string{
        "edb0478d-7436-11ea-86e6-0a58ac144b91",
    },
    Volumes:               []string{
        "ba49449a-7435-11ea-b89e-0a58ac14480f",
    },
}

resp, err := dropletsApi.DropletsDestroyWithAssociatedResourcesSelective(ctx, dropletId, &body)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.V21Clicks401Error:
            log.Fatalln("V21Clicks401ErrorException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    fmt.Println(resp.StatusCode)
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



