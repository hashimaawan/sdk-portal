# Volumes List

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkJsb2NrJTI1MjBTdG9yYWdlJTJGdm9sdW1lc19saXN0

To list all of the block storage volumes available on your account, send a GET request to `/v2/volumes`.

## Filtering Results

### By Region

The `region` may be provided as query parameter in order to restrict results to volumes available in a specific region. For example: `/v2/volumes?region=nyc1`

### By Name

It is also possible to list volumes on your account that match a specified name. To do so, send a GET request with the volume's name as a query parameter to `/v2/volumes?name=$VOLUME_NAME`.
**Note:** You can only create one volume per region with the same name.

### By Name and Region

It is also possible to retrieve information about a block storage volume by name. To do so, send a GET request with the volume's name and the region slug for the region it is located in as query parameters to `/v2/volumes?name=$VOLUME_NAME&region=nyc1`.

```ruby
def volumes_list(name: nil,
                 region: nil,
                 per_page: 20,
                 page: 1)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Query, Optional | The block storage volume's name. |
| `region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/region-2.md) | Query, Optional | The slug identifier for the region where the resource is available. |
| `per_page` | `Integer` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `Integer` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |


# Response Type

**200**: The response will be a JSON object with a key called `volumes`. This will be set to an array of volume objects, each of which will contain the standard volume attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2VolumesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-volumes-response.md).


# Example Usage

```ruby
name = 'example'

region = Region2::NYC3

per_page = 2

page = 1

result = block_storage_api.volumes_list(
  name: name,
  region: region,
  per_page: per_page,
  page: page
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
  "volumes": [
    {
      "created_at": "2016-03-02T17:00:49Z",
      "description": "Block store for examples",
      "droplet_ids": [],
      "filesystem_label": "example",
      "filesystem_type": "ext4",
      "id": "506f78a4-e098-11e5-ad9f-000f53306ae1",
      "name": "example",
      "region": {
        "available": true,
        "features": [
          "private_networking",
          "backups",
          "ipv6",
          "metadata"
        ],
        "name": "New York 1",
        "sizes": [
          "s-1vcpu-1gb",
          "s-1vcpu-2gb",
          "s-1vcpu-3gb",
          "s-2vcpu-2gb",
          "s-3vcpu-1gb",
          "s-2vcpu-4gb",
          "s-4vcpu-8gb",
          "s-6vcpu-16gb",
          "s-8vcpu-32gb",
          "s-12vcpu-48gb",
          "s-16vcpu-64gb",
          "s-20vcpu-96gb",
          "s-24vcpu-128gb",
          "s-32vcpu-192gb"
        ],
        "slug": "nyc1"
      },
      "size_gigabytes": 10,
      "tags": [
        "aninterestingtag"
      ]
    },
    {
      "created_at": "2016-03-02T17:01:49Z",
      "description": "Block store for examples",
      "droplet_ids": [],
      "filesystem_label": "example",
      "filesystem_type": "ext4",
      "id": "506f78a4-e098-11e5-ad9f-000f53305eb2",
      "name": "example",
      "region": {
        "available": true,
        "features": [
          "private_networking",
          "backups",
          "ipv6",
          "metadata"
        ],
        "name": "New York 3",
        "sizes": [
          "s-1vcpu-1gb",
          "s-1vcpu-2gb",
          "s-1vcpu-3gb",
          "s-2vcpu-2gb",
          "s-3vcpu-1gb",
          "s-2vcpu-4gb",
          "s-4vcpu-8gb",
          "s-6vcpu-16gb",
          "s-8vcpu-32gb",
          "s-12vcpu-48gb",
          "s-16vcpu-64gb",
          "s-20vcpu-96gb",
          "s-24vcpu-128gb",
          "s-32vcpu-192gb"
        ],
        "slug": "nyc3"
      },
      "size_gigabytes": 10,
      "tags": [
        "aninterestingtag"
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



