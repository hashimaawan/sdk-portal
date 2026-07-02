# Droplets Get Destroy Associated Resources Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkRyb3BsZXRzJTJGZHJvcGxldHNfZ2V0X0Rlc3Ryb3lBc3NvY2lhdGVkUmVzb3VyY2VzU3RhdHVz

To check on the status of a request to destroy a Droplet with its associated
resources, send a GET request to the
`/v2/droplets/$DROPLET_ID/destroy_with_associated_resources/status` endpoint.

```python
def droplets_get_destroy_associated_resources_status(self,
                                                    droplet_id)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet_id` | `int` | Template, Required | A unique identifier for a Droplet instance.<br><br>**Constraints**: `>= 1` |


# Response Type

**200**: A JSON object containing containing the status of a request to destroy a Droplet and its associated resources.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2DropletsDestroyWithAssociatedResourcesStatusResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-droplets-destroy-with-associated-resources-status-response.md).


# Example Usage

```python
droplet_id = 3164444

result = droplets_api.droplets_get_destroy_associated_resources_status(droplet_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "completed_at": "2020-04-01T18:11:49Z",
  "droplet": {
    "destroyed_at": "2020-04-01T18:11:49Z",
    "id": "187000742",
    "name": "ubuntu-s-1vcpu-1gb-nyc1-01"
  },
  "failures": 0,
  "resources": {
    "floating_ips": [
      {
        "destroyed_at": "2020-04-01T18:11:44Z",
        "id": "6186916",
        "name": "45.55.96.47"
      }
    ],
    "reserved_ips": [
      {
        "destroyed_at": "2020-04-01T18:11:44Z",
        "id": "6186916",
        "name": "45.55.96.47"
      }
    ],
    "snapshots": [
      {
        "destroyed_at": "2020-04-01T18:11:44Z",
        "id": "61486916",
        "name": "ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330"
      }
    ],
    "volume_snapshots": [
      {
        "destroyed_at": "2020-04-01T18:11:44Z",
        "id": "edb0478d-7436-11ea-86e6-0a58ac144b91",
        "name": "volume-nyc1-01-1585758983629"
      }
    ],
    "volumes": []
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



