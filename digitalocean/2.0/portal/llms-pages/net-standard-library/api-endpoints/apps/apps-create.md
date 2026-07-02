# Apps Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2NyZWF0ZQ

Create a new app by submitting an app specification. For documentation on app specifications (`AppSpec` objects), please refer to [the product documentation](https://docs.digitalocean.com/products/app-platform/reference/app-spec/).

```csharp
AppsCreateAsync(
    Models.V2AppsRequest body,
    Models.Accept? accept = null,
    Models.ContentType? contentType = null)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V2AppsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-apps-request.md) | Body, Required | - |
| `accept` | [`Accept?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/accept.md) | Header, Optional | The content-type that should be used by the response. By default, the response will be `application/json`. `application/yaml` is also supported. |
| `contentType` | [`ContentType?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/content-type.md) | Header, Optional | The content-type used for the request. By default, the requests are assumed to use `application/json`. `application/yaml` is also supported. |


# Response Type

**200**: A JSON or YAML of a `spec` object.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2AppsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-apps-response-1.md).


# Example Usage

```csharp
V2AppsRequest body = new V2AppsRequest
{
    Spec = new AppSpec
    {
        Name = "web-app",
        Region = Region1.Nyc,
        Services = new List<Service>
        {
            new Service
            {
                Name = "api",
                EnvironmentSlug = "node-js",
                Github = new Github
                {
                    Branch = "main",
                    DeployOnPush = true,
                    Repo = "digitalocean/sample-golang",
                },
                RunCommand = "bin/api",
                InstanceCount = 2L,
                InstanceSizeSlug = InstanceSizeSlug.Basicxxs,
                Routes = new List<ACriterionForRoutingHttpTrafficToAComponent>
                {
                    new ACriterionForRoutingHttpTrafficToAComponent
                    {
                        Path = "/api",
                    },
                },
            },
        },
    },
};

Accept? accept = Accept.EnumApplicationjson;
ContentType? contentType = ContentType.EnumApplicationjson;
try
{
    ApiResponse<V2AppsResponse1> result = await appsApi.AppsCreateAsync(
        body,
        accept,
        contentType
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is V21Clicks401ErrorException)
    {
       // TODO: Handle V21Clicks401ErrorException exception here
    }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



