# Snapshots List

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRlNuYXBzaG90cyUyRnNuYXBzaG90c19saXN0

To list all of the snapshots available on your account, send a GET request to
`/v2/snapshots`.

The response will be a JSON object with a key called `snapshots`. This will be
set to an array of `snapshot` objects, each of which will contain the standard
snapshot attributes.

### Filtering Results by Resource Type

It's possible to request filtered results by including certain query parameters.

#### List Droplet Snapshots

To retrieve only snapshots based on Droplets, include the `resource_type`
query parameter set to `droplet`. For example, `/v2/snapshots?resource_type=droplet`.

#### List Volume Snapshots

To retrieve only snapshots based on volumes, include the `resource_type`
query parameter set to `volume`. For example, `/v2/snapshots?resource_type=volume`.

```ruby
def snapshots_list(per_page: 20,
                   page: 1,
                   resource_type: nil)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `per_page` | `Integer` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `Integer` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |
| `resource_type` | [`ResourceType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/resource-type.md) | Query, Optional | Used to filter snapshots by a resource type. |


# Response Type

**200**: A JSON object with a key of `snapshots`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2SnapshotsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-snapshots-response.md).


# Example Usage

```ruby
per_page = 2

page = 1

resource_type = ResourceType::DROPLET

result = snapshots_api.snapshots_list(
  per_page: per_page,
  page: page,
  resource_type: resource_type
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Example Response *(as JSON)*

```json
{
  "links": {},
  "meta": {
    "total": 2
  },
  "snapshots": [
    {
      "created_at": "2020-07-28T16:47:44Z",
      "id": "6372321",
      "min_disk_size": 25,
      "name": "web-01-1595954862243",
      "regions": [
        "nyc3",
        "sfo3"
      ],
      "resource_id": "200776916",
      "resource_type": "droplet",
      "size_gigabytes": 2.34,
      "tags": [
        "web",
        "env:prod"
      ]
    },
    {
      "created_at": "2019-09-28T23:14:30Z",
      "id": "fbe805e8-866b-11e6-96bf-000f53315a41",
      "min_disk_size": 2,
      "name": "pvc-01-1595954862243",
      "regions": [
        "nyc1"
      ],
      "resource_id": "89bcc42f-85cf-11e6-a004-000f53315871",
      "resource_type": "volume",
      "size_gigabytes": 0.1008,
      "tags": [
        "k8s"
      ]
    }
  ]
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |



