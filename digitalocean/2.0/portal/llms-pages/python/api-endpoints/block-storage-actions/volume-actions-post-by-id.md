# Volume Actions Post by Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkJsb2NrJTI1MjBTdG9yYWdlJTI1MjBBY3Rpb25zJTJGdm9sdW1lQWN0aW9uc19wb3N0X2J5SWQ

To initiate an action on a block storage volume by Id, send a POST request to
`~/v2/volumes/$VOLUME_ID/actions`. The body should contain the appropriate
attributes for the respective action.

## Attach a Block Storage Volume to a Droplet

| Attribute  | Details                                                             |
| ---------- | ------------------------------------------------------------------- |
| type       | This must be `attach`                                               |
| droplet_id | Set to the Droplet's ID                                             |
| region     | Set to the slug representing the region where the volume is located |

Each volume may only be attached to a single Droplet. However, up to seven
volumes may be attached to a Droplet at a time. Pre-formatted volumes will be
automatically mounted to Ubuntu, Debian, Fedora, Fedora Atomic, and CentOS
Droplets created on or after April 26, 2018 when attached. On older Droplets,
[additional configuration](https://www.digitalocean.com/community/tutorials/how-to-partition-and-format-digitalocean-block-storage-volumes-in-linux#mounting-the-filesystems)
is required.

## Remove a Block Storage Volume from a Droplet

| Attribute  | Details                                                             |
| ---------- | ------------------------------------------------------------------- |
| type       | This must be `detach`                                               |
| droplet_id | Set to the Droplet's ID                                             |
| region     | Set to the slug representing the region where the volume is located |

## Resize a Volume

| Attribute      | Details                                                             |
| -------------- | ------------------------------------------------------------------- |
| type           | This must be `resize`                                               |
| size_gigabytes | The new size of the block storage volume in GiB (1024^3)            |
| region         | Set to the slug representing the region where the volume is located |

Volumes may only be resized upwards. The maximum size for a volume is 16TiB.

```python
def volume_actions_post_by_id(self,
                             volume_id,
                             body,
                             per_page=20,
                             page=1)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `volume_id` | `uuid\|str` | Template, Required | The ID of the block storage volume. |
| `body` | [V2 Volumes Actions Request](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-volumes-actions-request.md) \| [V2 Volumes Actions Request1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-volumes-actions-request-1.md) \| [V2 Volumes Actions Request2](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-volumes-actions-request-2.md) | Body, Required | This is a container for any-of cases. |
| `per_page` | `int` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `int` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |


# Response Type

**202**: The response will be an object with a key called `action`. The value of this will be an object that contains the standard volume action attributes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2VolumesActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-volumes-actions-response.md).


# Example Usage

```python
volume_id = '7724db7c-e098-11e5-b522-000f53304e51'

body = V2VolumesActionsRequest(
    mtype=Type21.ATTACH,
    droplet_id=11612190,
    region=Region2.NYC1,
    tags=[
        'aninterestingtag'
    ]
)

result = block_storage_actions_api.volume_actions_post_by_id(
    volume_id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "completed_at": null,
    "id": 68212773,
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
    "region_slug": "nyc1",
    "resource_id": null,
    "resource_type": "backend",
    "started_at": "2015-10-15T17:46:15Z",
    "status": "in-progress",
    "type": "detach_volume"
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



