# Apps Create Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2NyZWF0ZV9kZXBsb3ltZW50

Creating an app deployment will pull the latest changes from your repository and schedule a new deployment for your app.

```php
function appsCreateDeployment(string $appId, V2AppsDeploymentsRequest $body): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appId` | `string` | Template, Required | The app ID |
| `body` | [`V2AppsDeploymentsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-apps-deployments-request.md) | Body, Required | - |


# Response Type

**200**: A JSON object with a `deployment` key.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2AppsDeploymentsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-apps-deployments-response-1.md).


# Example Usage

```php
$appId = '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf';

$body = V2AppsDeploymentsRequestBuilder::init()
    ->forceBuild(true)
    ->build();

$appsApi = $client->getAppsApi();
$apiResponse = $appsApi->appsCreateDeployment(
    $appId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2AppsDeploymentsResponse1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



