# Databases List Options

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19saXN0X29wdGlvbnM

To list all of the options available for the offered database engines, send a GET request to `/v2/databases/options`.
The result will be a JSON object with an `options` key.

```python
def databases_list_options(self)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Response Type

**200**: A JSON string with a key of `options`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2DatabasesOptionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-databases-options-response.md).


# Example Usage

```python
result = databases_api.databases_list_options()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "options": {
    "mongodb": {
      "layouts": [
        {
          "num_nodes": 1,
          "sizes": [
            "db-s-1vcpu-1gb",
            "db-s-1vcpu-2gb"
          ]
        },
        {
          "num_nodes": 3,
          "sizes": [
            "db-s-1vcpu-1gb",
            "db-s-1vcpu-2gb",
            "db-s-2vcpu-4gb",
            "db-s-4vcpu-8gb"
          ]
        }
      ],
      "regions": [
        "ams3",
        "blr1"
      ],
      "versions": [
        "4.4",
        "5.0"
      ]
    },
    "mysql": {
      "layouts": [
        {
          "num_nodes": 1,
          "sizes": [
            "db-s-1vcpu-1gb",
            "db-s-1vcpu-2gb"
          ]
        },
        {
          "num_nodes": 2,
          "sizes": [
            "db-s-1vcpu-1gb",
            "db-s-1vcpu-2gb",
            "db-s-2vcpu-4gb",
            "db-s-4vcpu-8gb"
          ]
        },
        {
          "num_nodes": 3,
          "sizes": [
            "db-s-1vcpu-1gb",
            "db-s-1vcpu-2gb",
            "db-s-2vcpu-4gb",
            "db-s-4vcpu-8gb"
          ]
        }
      ],
      "regions": [
        "ams3",
        "blr1"
      ],
      "versions": [
        "8"
      ]
    },
    "pg": {
      "layouts": [
        {
          "num_nodes": 1,
          "sizes": [
            "db-s-1vcpu-1gb",
            "db-s-1vcpu-2gb"
          ]
        },
        {
          "num_nodes": 2,
          "sizes": [
            "db-s-1vcpu-1gb",
            "db-s-1vcpu-2gb",
            "db-s-2vcpu-4gb",
            "db-s-4vcpu-8gb"
          ]
        }
      ],
      "regions": [
        "ams3",
        "blr1"
      ],
      "versions": [
        "11",
        "12",
        "13",
        "14"
      ]
    },
    "redis": {
      "layouts": [
        {
          "num_nodes": 1,
          "sizes": [
            "db-s-1vcpu-1gb",
            "db-s-1vcpu-2gb"
          ]
        },
        {
          "num_nodes": 2,
          "sizes": [
            "db-s-1vcpu-1gb",
            "db-s-1vcpu-2gb",
            "db-s-2vcpu-4gb",
            "db-s-4vcpu-8gb"
          ]
        }
      ],
      "regions": [
        "ams3",
        "blr1"
      ],
      "versions": [
        "6"
      ]
    }
  },
  "version_availability": {
    "mongodb": [
      {
        "end_of_availability": "null",
        "end_of_life": "2024-02-01T08:00:00Z",
        "version": "4.4"
      },
      {
        "end_of_availability": "null",
        "end_of_life": "2024-10-01T07:00:00Z",
        "version": "5.0"
      }
    ],
    "mysql": [
      {
        "end_of_availability": "null",
        "end_of_life": "null",
        "version": "8"
      }
    ],
    "pg": [
      {
        "end_of_availability": "2023-05-09T00:00:00Z",
        "end_of_life": "2023-11-09T00:00:00Z",
        "version": "11"
      },
      {
        "end_of_availability": "2024-05-14T00:00:00Z",
        "end_of_life": "2024-11-14T00:00:00Z",
        "version": "12"
      },
      {
        "end_of_availability": "2025-05-13T00:00:00Z",
        "end_of_life": "2025-11-13T00:00:00Z",
        "version": "13"
      },
      {
        "end_of_availability": "2026-05-12T00:00:00Z",
        "end_of_life": "2026-11-12T00:00:00Z",
        "version": "14"
      }
    ],
    "redis": [
      {
        "end_of_availability": "null",
        "end_of_life": "null",
        "version": "7"
      }
    ]
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



