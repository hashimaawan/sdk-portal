# Cdn Update Endpoints

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkNETiUyNTIwRW5kcG9pbnRzJTJGY2RuX3VwZGF0ZV9lbmRwb2ludHM

To update the TTL, certificate ID, or the FQDN of the custom subdomain for
an existing CDN endpoint, send a PUT request to
`/v2/cdn/endpoints/$ENDPOINT_ID`.

```go
CdnUpdateEndpoints(
    ctx context.Context,
    cdnId uuid.UUID,
    body models.V2CdnEndpointsRequest) (
    models.ApiResponse[models.V2CdnEndpointsResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cdnId` | `uuid.UUID` | Template, Required | A unique identifier for a CDN endpoint. |
| `body` | [`models.V2CdnEndpointsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-cdn-endpoints-request.md) | Body, Required | - |


# Response Type

**200**: The response will be a JSON object with an `endpoint` key. This will be set to an object containing the standard CDN endpoint attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2CdnEndpointsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-cdn-endpoints-response-1.md).


# Example Usage

```go
ctx := context.Background()

cdnId := uuid.MustParse("19f06b6a-3ace-4315-b086-499a0e521b76")

body := models.V2CdnEndpointsRequest{
    CertificateId:         models.ToPointer(uuid.MustParse("892071a0-bb95-49bc-8021-3afd67a210bf")),
    CustomDomain:          models.ToPointer("static.example.com"),
    Ttl:                   models.ToPointer(models.Ttl_Enum3600),
}

apiResponse, err := cdnEndpointsApi.CdnUpdateEndpoints(ctx, cdnId, body)
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
  "endpoint": {
    "created_at": "2018-07-19T15:04:16Z",
    "endpoint": "static-images.nyc3.cdn.digitaloceanspaces.com",
    "id": "19f06b6a-3ace-4315-b086-499a0e521b76",
    "origin": "static-images.nyc3.digitaloceanspaces.com",
    "ttl": 3600
  }
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



