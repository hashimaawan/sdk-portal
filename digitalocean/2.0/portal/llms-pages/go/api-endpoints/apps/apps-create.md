# Apps Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2NyZWF0ZQ

Create a new app by submitting an app specification. For documentation on app specifications (`AppSpec` objects), please refer to [the product documentation](https://docs.digitalocean.com/products/app-platform/reference/app-spec/).

```go
AppsCreate(
    ctx context.Context,
    body models.V2AppsRequest,
    accept *models.Accept,
    contentType *models.ContentType) (
    models.ApiResponse[models.V2AppsResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`models.V2AppsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-apps-request.md) | Body, Required | - |
| `accept` | [`*models.Accept`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/accept.md) | Header, Optional | The content-type that should be used by the response. By default, the response will be `application/json`. `application/yaml` is also supported. |
| `contentType` | [`*models.ContentType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/content-type.md) | Header, Optional | The content-type used for the request. By default, the requests are assumed to use `application/json`. `application/yaml` is also supported. |


# Response Type

**200**: A JSON or YAML of a `spec` object.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2AppsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-apps-response-1.md).


# Example Usage

```go
ctx := context.Background()

body := models.V2AppsRequest{
    Spec:                  models.AppSpec{
        Name:                  "web-app",
        Region:                models.ToPointer(models.Region1_Nyc),
        Services:              []models.Service{
            models.Service{
                EnvironmentSlug:       models.ToPointer("node-js"),
                Github:                models.ToPointer(models.Github{
                    Branch:                models.ToPointer("main"),
                    DeployOnPush:          models.ToPointer(true),
                    Repo:                  models.ToPointer("digitalocean/sample-golang"),
                }),
                Name:                  "api",
                RunCommand:            models.ToPointer("bin/api"),
                InstanceCount:         models.ToPointer(int64(2)),
                InstanceSizeSlug:      models.ToPointer(models.InstanceSizeSlug_Basicxxs),
                Routes:                []models.ACriterionForRoutingHttpTrafficToAComponent{
                    models.ACriterionForRoutingHttpTrafficToAComponent{
                        Path:                  models.ToPointer("/api"),
                    },
                },
            },
        },
    },
}

accept := models.Accept_EnumApplicationjson

contentType := models.ContentType_EnumApplicationjson

apiResponse, err := appsApi.AppsCreate(ctx, body, &accept, &contentType)
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
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



