# Apps List Deployments

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2xpc3RfZGVwbG95bWVudHM

List all deployments of an app.

```python
def apps_list_deployments(self,
                         app_id,
                         page=1,
                         per_page=20)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_id` | `str` | Template, Required | The app ID |
| `page` | `int` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |
| `per_page` | `int` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |


# Response Type

**200**: A JSON object with a `deployments` key. This will be a list of all app deployments

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2AppsDeploymentsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-apps-deployments-response.md).


# Example Usage

```python
app_id = '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf'

page = 1

per_page = 2

result = apps_api.apps_list_deployments(
    app_id,
    page=page,
    per_page=per_page
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "deployments": [
    {
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
  ],
  "links": {
    "pages": {}
  },
  "meta": {
    "total": 1
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |



