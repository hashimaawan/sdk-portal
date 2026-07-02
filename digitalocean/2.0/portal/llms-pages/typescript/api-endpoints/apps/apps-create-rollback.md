# Apps Create Rollback

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2NyZWF0ZV9yb2xsYmFjaw

Rollback an app to a previous deployment. A new deployment will be created to perform the rollback.
The app will be pinned to the rollback deployment preventing any new deployments from being created,
either manually or through Auto Deploy on Push webhooks. To resume deployments, the rollback must be
either committed or reverted.

It is recommended to use the Validate App Rollback endpoint to double check if the rollback is
valid and if there are any warnings.

```ts
async appsCreateRollback(
  appId: string,
  body: V2AppsRollbackRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2AppsDeploymentsResponse1>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appId` | `string` | Template, Required | The app ID |
| `body` | [`V2AppsRollbackRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-apps-rollback-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A JSON object with a `deployment` key.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2AppsDeploymentsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-apps-deployments-response-1.md).


# Example Usage

```ts
const appId = '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf';

const body: V2AppsRollbackRequest = {
  deploymentId: '3aa4d20e-5527-4c00-b496-601fbd22520a',
  skipPin: false,
};

try {
  const response = await appsApi.appsCreateRollback(
    appId,
    body
  );

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
  "deployment": {
    "cause": "commit 9a4df0b pushed to github/digitalocean/sample-golang",
    "created_at": "2020-07-28T18:00:00Z",
    "id": "b6bdf840-2854-4f87-a36c-5f231c617c84",
    "phase": "PENDING_BUILD",
    "phase_last_updated_at": "0001-01-01T00:00:00Z",
    "progress": {
      "pending_steps": 6,
      "steps": [
        {
          "name": "build",
          "status": "PENDING",
          "steps": [
            {
              "name": "initialize",
              "status": "PENDING"
            },
            {
              "name": "components",
              "status": "PENDING",
              "steps": [
                {
                  "component_name": "web",
                  "message_base": "Building service",
                  "name": "web",
                  "status": "PENDING"
                }
              ]
            }
          ]
        },
        {
          "name": "deploy",
          "status": "PENDING",
          "steps": [
            {
              "name": "initialize",
              "status": "PENDING"
            },
            {
              "name": "components",
              "status": "PENDING",
              "steps": [
                {
                  "component_name": "web",
                  "name": "web",
                  "status": "PENDING",
                  "steps": [
                    {
                      "component_name": "web",
                      "message_base": "Deploying service",
                      "name": "deploy",
                      "status": "PENDING"
                    },
                    {
                      "component_name": "web",
                      "message_base": "Waiting for service",
                      "name": "wait",
                      "status": "PENDING"
                    }
                  ]
                }
              ]
            },
            {
              "name": "finalize",
              "status": "PENDING"
            }
          ]
        }
      ],
      "total_steps": 6
    },
    "services": [
      {
        "name": "web",
        "source_commit_hash": "9a4df0b8e161e323bc3cdf1dc71878080fe144fa"
      }
    ],
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
          "instance_count": 2,
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
    },
    "tier_slug": "basic",
    "updated_at": "2020-07-28T18:00:00Z"
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



