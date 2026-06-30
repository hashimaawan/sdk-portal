# Update an Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0ZSUyRkltYWdlcyUyRlVwZGF0ZSUyNTIwYW4lMjUyMEltYWdl

Updates the Image. You may change the description, convert a Backup Image to a Snapshot Image or change the Image labels. Only Images of type `snapshot` and `backup` can be updated.

Note that when updating labels, the current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def update_an_image(id,
                    body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Image |
| `body` | [`UpdateImageRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/update-image-request.md) | Body, Optional | - |


# Response Type

**200**: The image key in the reply contains the modified Image object

[`ImagesResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/images-response-1.md)


# Example Usage

```ruby
id = 112

body = UpdateImageRequest.new(
  'My new Image description',
  { 'labelkey' => 'value' },
  envrr
)

result = images_controller.update_an_image(
  id,
  body: body
)
puts result
```


# Example Response *(as JSON)*

```json
{
  "image": {
    "bound_to": null,
    "build_id": "c313fe40383af26094a5a92026054320ab55abc7",
    "created": "2016-01-30T23:50:00+00:00",
    "created_from": {
      "id": 1,
      "name": "Server"
    },
    "deleted": null,
    "deprecated": "2018-02-28T00:00:00+00:00",
    "description": "My new Image description",
    "disk_size": 10,
    "id": 4711,
    "image_size": 2.3,
    "labels": {
      "labelkey": "value"
    },
    "name": null,
    "os_flavor": "ubuntu",
    "os_version": "20.04",
    "protection": {
      "delete": false
    },
    "rapid_deploy": false,
    "status": "available",
    "type": "snapshot"
  }
}
```



