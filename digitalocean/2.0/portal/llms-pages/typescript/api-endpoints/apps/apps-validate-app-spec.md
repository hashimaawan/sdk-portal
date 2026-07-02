# Apps Validate App Spec

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX3ZhbGlkYXRlX2FwcFNwZWM

To propose and validate a spec for a new or existing app, send a POST request to the `/v2/apps/propose` endpoint. The request returns some information about the proposed app, including app cost and upgrade cost. If an existing app ID is specified, the app spec is treated as a proposed update to the existing app.

```ts
async appsValidateAppSpec(
  body: V2AppsProposeRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2AppsProposeResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V2AppsProposeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-apps-propose-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A JSON object.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2AppsProposeResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-apps-propose-response.md).


# Example Usage

```ts
const body: V2AppsProposeRequest = {
  spec: {
    name: 'web-app',
    region: Region1.Nyc,
    services: [
      {
        name: 'api',
        environmentSlug: 'node-js',
        github: {
          branch: 'main',
          deployOnPush: true,
          repo: 'digitalocean/sample-golang',
        },
        runCommand: 'bin/api',
        instanceCount: BigInt(2),
        instanceSizeSlug: InstanceSizeSlug.Basicxxs,
        routes: [
          {
            path: '/api',
          }
        ],
      }
    ],
  },
  appId: 'b6bdf840-2854-4f87-a36c-5f231c617c84',
};

try {
  const response = await appsApi.appsValidateAppSpec(body);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
    if (error instanceof V21Clicks401Error) {
      console.log(error.result);
    }
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
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



