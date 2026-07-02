# Apps Cancel Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2NhbmNlbF9kZXBsb3ltZW50

Immediately cancel an in-progress deployment.

```java
CompletableFuture<ApiResponse<V2AppsDeploymentsResponse1>> appsCancelDeploymentAsync(
    final String appId,
    final String deploymentId)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appId` | `String` | Template, Required | The app ID |
| `deploymentId` | `String` | Template, Required | The deployment ID |


# Response Type

**200**: A JSON the `deployment` that was just cancelled.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2AppsDeploymentsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-apps-deployments-response-1.md).


# Example Usage

```java
String appId = "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf";
String deploymentId = "3aa4d20e-5527-4c00-b496-601fbd22520a";

appsApi.appsCancelDeploymentAsync(appId, deploymentId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof V21Clicks401ErrorException) {
        V21Clicks401ErrorException v21Clicks401ErrorException = (V21Clicks401ErrorException) cause;
        v21Clicks401ErrorException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



