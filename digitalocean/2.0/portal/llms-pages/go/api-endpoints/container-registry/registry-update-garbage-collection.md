# Registry Update Garbage Collection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkNvbnRhaW5lciUyNTIwUmVnaXN0cnklMkZyZWdpc3RyeV91cGRhdGVfZ2FyYmFnZUNvbGxlY3Rpb24

To cancel the currently-active garbage collection for a registry, send a PUT request to `/v2/registry/$REGISTRY_NAME/garbage-collection/$GC_UUID` and specify one or more of the attributes below.

```go
RegistryUpdateGarbageCollection(
    ctx context.Context,
    registryName string,
    garbageCollectionUuid string,
    body models.V2RegistryGarbageCollectionRequest) (
    models.ApiResponse[models.V2RegistryGarbageCollectionResponse],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `registryName` | `string` | Template, Required | The name of a container registry. |
| `garbageCollectionUuid` | `string` | Template, Required | The UUID of a garbage collection run. |
| `body` | [`models.V2RegistryGarbageCollectionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-registry-garbage-collection-request.md) | Body, Required | - |


# Response Type

**200**: The response will be a JSON object with a key of `garbage_collection`. This will be a json object with attributes representing the currently-active garbage collection.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2RegistryGarbageCollectionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-registry-garbage-collection-response.md).


# Example Usage

```go
ctx := context.Background()

registryName := "example"

garbageCollectionUuid := "eff0feee-49c7-4e8f-ba5c-a320c109c8a8"

body := models.V2RegistryGarbageCollectionRequest{
    Cancel:                models.ToPointer(true),
}

apiResponse, err := containerRegistryApi.RegistryUpdateGarbageCollection(ctx, registryName, garbageCollectionUuid, body)
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



