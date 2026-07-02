# Apps Validate App Spec

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX3ZhbGlkYXRlX2FwcFNwZWM

To propose and validate a spec for a new or existing app, send a POST request to the `/v2/apps/propose` endpoint. The request returns some information about the proposed app, including app cost and upgrade cost. If an existing app ID is specified, the app spec is treated as a proposed update to the existing app.

```csharp
AppsValidateAppSpecAsync(
    Models.V2AppsProposeRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V2AppsProposeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-apps-propose-request.md) | Body, Required | - |


# Response Type

**200**: A JSON object.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2AppsProposeResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-apps-propose-response.md).


# Example Usage

```csharp
V2AppsProposeRequest body = new V2AppsProposeRequest
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
    AppId = "b6bdf840-2854-4f87-a36c-5f231c617c84",
};

try
{
    ApiResponse<V2AppsProposeResponse> result = await appsApi.AppsValidateAppSpecAsync(body);
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


# Example Response *(as JSON)*

```json
{
  "app_cost": 5,
  "app_name_available": true,
  "app_tier_upgrade_cost": 17,
  "existing_static_apps": "2",
  "max_free_static_apps": "3",
  "spec": {
    "name": "sample-golang",
    "region": "ams",
    "services": [
      {
        "environment_slug": "go",
        "github": {
          "branch": "branch",
          "repo": "digitalocean/sample-golang"
        },
        "http_port": 8080,
        "instance_count": 1,
        "instance_size_slug": "basic-xxs",
        "name": "web",
        "routes": [
          {
            "path": "/"
          }
        ],
        "run_command": "bin/sample-golang"
      }
    ]
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



