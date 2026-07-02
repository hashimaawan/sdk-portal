# Cdn Create Endpoint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkNETiUyNTIwRW5kcG9pbnRzJTJGY2RuX2NyZWF0ZV9lbmRwb2ludA

To create a new CDN endpoint, send a POST request to `/v2/cdn/endpoints`. The
origin attribute must be set to the fully qualified domain name (FQDN) of a
DigitalOcean Space. Optionally, the TTL may be configured by setting the `ttl`
attribute.

A custom subdomain may be configured by specifying the `custom_domain` and
`certificate_id` attributes.

```go
CdnCreateEndpoint(
    ctx context.Context,
    body models.Endpoint) (
    models.ApiResponse[models.V2CdnEndpointsResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`models.Endpoint`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/endpoint.md) | Body, Required | - |


# Response Type

**201**: The response will be a JSON object with an `endpoint` key. This will be set to an object containing the standard CDN endpoint attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2CdnEndpointsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-cdn-endpoints-response-1.md).


# Example Usage

```go
ctx := context.Background()

body := models.Endpoint{
    Origin:                "static-images.nyc3.digitaloceanspaces.com",
    Ttl:                   models.ToPointer(models.Ttl_Enum3600),
}

apiResponse, err := cdnEndpointsApi.CdnCreateEndpoint(ctx, body)
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
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



