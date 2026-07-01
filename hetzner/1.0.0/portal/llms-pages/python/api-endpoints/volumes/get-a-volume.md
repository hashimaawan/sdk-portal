# Get a Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZHZXQlMjUyMGElMjUyMFZvbHVtZQ

Gets a specific Volume object.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_a_volume(self,
                id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Volume |


# Response Type

**200**: The `volume` key contains the volume

[`VolumesResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/volumes-response-2.md)


# Example Usage

```python
id = 112

result = volumes_controller.get_a_volume(id)
print(result)
```



