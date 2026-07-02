# Apps List

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2xpc3Q

List all apps on your account. Information about the current active deployment as well as any in progress ones will also be included for each app.

```ts
async appsList(
  page?: number,
  perPage?: number,
  withProjects?: boolean,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2AppsResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `number \| undefined` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |
| `perPage` | `number \| undefined` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `withProjects` | `boolean \| undefined` | Query, Optional | Whether the project_id of listed apps should be fetched and included. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A JSON object with a `apps` key. This is list of object `apps`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2AppsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-apps-response.md).


# Example Usage

```ts
const page = 1;

const perPage = 2;

const withProjects = true;

try {
  const response = await appsApi.appsList(
    page,
    perPage,
    withProjects
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
  "apps": [
    {
      "active_deployment": {
        "created_at": "2020-12-01T00:40:05Z",
        "id": "3aa4d20e-5527-4c00-b496-601fbd22520a",
        "phase_last_updated_at": "2020-12-01T00:42:12Z",
        "services": [
          {
            "name": "sample-php",
            "source_commit_hash": "54d4a727f457231062439895000d45437c7bb405"
          }
        ],
        "spec": {
          "domains": [
            {
              "domain": "sample-php.example.com",
              "minimum_tls_version": "1.3",
              "type": "PRIMARY",
              "zone": "example.com"
            }
          ],
          "name": "sample-php",
          "region": "fra",
          "services": [
            {
              "environment_slug": "php",
              "git": {
                "branch": "main",
                "repo_clone_url": "https://github.com/digitalocean/sample-php.git"
              },
              "http_port": 8080,
              "instance_count": 1,
              "instance_size_slug": "basic-xxs",
              "name": "sample-php",
              "routes": [
                {
                  "path": "/"
                }
              ],
              "run_command": "heroku-php-apache2"
            }
          ]
        },
        "updated_at": "2020-12-01T00:42:12Z"
      },
      "cause": "app spec updated",
      "created_at": "2020-11-19T20:27:18Z",
      "default_ingress": "https://sample-php-iaj87.ondigitalocean.app",
      "domains": [
        {
          "certificate_expires_at": "2024-01-29T23:59:59Z",
          "id": "0831f444-a1a7-11ed-828c-ef59494480b5",
          "phase": "ACTIVE",
          "progress": {
            "steps": [
              {
                "ended_at": "0001-01-01T00:00:00Z",
                "name": "default-ingress-ready",
                "started_at": "2023-01-30T22:15:45.021896292Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "0001-01-01T00:00:00Z",
                "name": "ensure-zone",
                "started_at": "2023-01-30T22:15:45.022017004Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "2023-01-30T15:42:28.50752065Z",
                "name": "ensure-ns-records",
                "started_at": "2023-01-30T22:15:45.025567874Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "0001-01-01T00:00:00Z",
                "name": "verify-nameservers",
                "started_at": "2023-01-30T22:15:45.033591906Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "0001-01-01T00:00:00Z",
                "name": "ensure-record",
                "started_at": "2023-01-30T22:15:45.156750604Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "2023-01-30T15:43:30.258626422Z",
                "name": "ensure-alias-record",
                "started_at": "2023-01-30T22:15:45.165933869Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "2023-01-30T15:43:30.258808279Z",
                "name": "ensure-wildcard-record",
                "started_at": "2023-01-30T22:15:45.166093422Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "0001-01-01T00:00:00Z",
                "name": "verify-cname",
                "started_at": "2023-01-30T22:15:45.166205559Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "2023-01-30T15:43:30.475903785Z",
                "name": "ensure-ssl-txt-record-saved",
                "started_at": "2023-01-30T22:15:45.295237186Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "2023-01-30T15:43:30.476017236Z",
                "name": "ensure-ssl-txt-record",
                "started_at": "2023-01-30T22:15:45.295315291Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "2023-01-30T15:43:30.476094058Z",
                "name": "ensure-renewal-email",
                "started_at": "2023-01-30T22:15:45.295374087Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "0001-01-01T00:00:00Z",
                "name": "ensure-CA-authorization",
                "started_at": "2023-01-30T22:15:45.295428101Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "0001-01-01T00:00:00Z",
                "name": "ensure-certificate",
                "started_at": "2023-01-30T22:15:45.978756406Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "2023-01-30T15:43:52.570612857Z",
                "name": "create-deployment",
                "started_at": "0001-01-01T00:00:00Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "2023-01-30T15:43:31.333582377Z",
                "name": "configuration-alert",
                "started_at": "2023-01-30T22:15:46.278987808Z",
                "status": "SUCCESS"
              }
            ]
          },
          "rotate_validation_records": false,
          "spec": {
            "domain": "sample-php.example.com",
            "minimum_tls_version": "1.3",
            "type": "PRIMARY",
            "zone": "example.com"
          }
        }
      ],
      "id": "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
      "last_deployment_created_at": "2020-12-01T00:40:05Z",
      "live_domain": "sample-php.example.com",
      "live_url": "https://sample-php.example.com",
      "live_url_base": "https://sample-php.example.com",
      "owner_uuid": "ff36cbc6fd350fe12577f5123133bb5ba01a2419",
      "pending_deployment": {
        "created_at": "2020-12-01T00:40:05Z",
        "id": "3aa4d20e-5527-4c00-b496-601fbd22520a",
        "phase_last_updated_at": "2020-12-01T00:42:12Z",
        "services": [
          {
            "name": "sample-php",
            "source_commit_hash": "54d4a727f457231062439895000d45437c7bb405"
          }
        ],
        "spec": {
          "domains": [
            {
              "domain": "sample-php.example.com",
              "minimum_tls_version": "1.3",
              "type": "PRIMARY",
              "zone": "example.com"
            }
          ],
          "name": "sample-php",
          "region": "fra",
          "services": [
            {
              "environment_slug": "php",
              "git": {
                "branch": "main",
                "repo_clone_url": "https://github.com/digitalocean/sample-php.git"
              },
              "http_port": 8080,
              "instance_count": 1,
              "instance_size_slug": "basic-xxs",
              "name": "sample-php",
              "routes": [
                {
                  "path": "/"
                }
              ],
              "run_command": "heroku-php-apache2"
            }
          ]
        },
        "updated_at": "2020-12-01T00:42:12Z"
      },
      "progress": {
        "phase": "ACTIVE",
        "steps": [
          {
            "ended_at": "2020-12-01T00:41:26.653989756Z",
            "name": "build",
            "started_at": "2020-12-01T00:40:11.979257919Z",
            "status": "SUCCESS",
            "steps": [
              {
                "ended_at": "2020-12-01T00:40:12.470972033Z",
                "name": "initialize",
                "started_at": "2020-12-01T00:40:11.979305214Z",
                "status": "SUCCESS"
              },
              {
                "ended_at": "2020-12-01T00:41:26.180360487Z",
                "name": "components",
                "started_at": "2020-12-01T00:40:12.470996857Z",
                "status": "SUCCESS",
                "steps": [
                  {
                    "component_name": "sample-php",
                    "ended_at": "0001-01-01T00:00:00Z",
                    "message_base": "Building service",
                    "name": "sample-php",
                    "started_at": "0001-01-01T00:00:00Z",
                    "status": "SUCCESS"
                  }
                ]
              }
            ]
          }
        ],
        "success_steps": 6,
        "tier_slug": "basic",
        "total_steps": 6
      },
      "region": {
        "continent": "Europe",
        "data_centers": [
          "fra1"
        ],
        "flag": "germany",
        "label": "Frankfurt",
        "slug": "fra"
      },
      "spec": {
        "domains": [
          {
            "domain": "sample-php.example.com",
            "minimum_tls_version": "1.3",
            "type": "PRIMARY",
            "zone": "example.com"
          }
        ],
        "name": "sample-php",
        "services": [
          {
            "environment_slug": "php",
            "git": {
              "branch": "main",
              "repo_clone_url": "https://github.com/digitalocean/sample-php.git"
            },
            "http_port": 8080,
            "instance_count": 1,
            "instance_size_slug": "basic-xxs",
            "name": "sample-php",
            "routes": [
              {
                "path": "/"
              }
            ],
            "run_command": "heroku-php-apache2"
          }
        ]
      },
      "tier_slug": "basic",
      "updated_at": "2020-12-01T00:42:16Z"
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
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



