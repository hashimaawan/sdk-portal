# Delete an Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkltYWdlcyUyRkRlbGV0ZSUyNTIwYW4lMjUyMEltYWdl

Deletes an Image. Only Images of type `snapshot` and `backup` can be deleted.

:information_source: **Note** This endpoint does not require authentication.

```python
def delete_an_image(self,
                   id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Image |


# Response Type

**204**: Image deleted

`void`


# Example Usage

```python
id = 112

images_controller.delete_an_image(id)
```



