# Update a Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZVcGRhdGUlMjUyMGElMjUyMFZvbHVtZQ

Updates the Volume properties.

Note that when updating labels, the volume’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```csharp
UpdateAVolumeAsync(
    string id,
    Models.UpdateVolumeRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | ID of the Volume to update |
| `body` | [`UpdateVolumeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/update-volume-request.md) | Body, Optional | - |


# Response Type

**200**: The `volume` key contains the updated volume

[`Task<Models.VolumesResponse2>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/volumes-response-2.md)


# Example Usage

```csharp
string id = "id0";
UpdateVolumeRequest body = new UpdateVolumeRequest
{
    Name = "database-storage",
};

try
{
    VolumesResponse2 result = await volumesController.UpdateAVolumeAsync(
        id,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Example Response *(as JSON)*

```json
{
  "volume": {
    "created": "2016-01-30T23:50:11+00:00",
    "format": "xfs",
    "id": 4711,
    "labels": {
      "labelkey": "value"
    },
    "linux_device": "/dev/disk/by-id/scsi-0HC_Volume_4711",
    "location": {
      "city": "Falkenstein",
      "country": "DE",
      "description": "Falkenstein DC Park 1",
      "id": 1,
      "latitude": 50.47612,
      "longitude": 12.370071,
      "name": "fsn1",
      "network_zone": "eu-central"
    },
    "name": "database-storage",
    "protection": {
      "delete": false
    },
    "server": 12,
    "size": 42,
    "status": "available"
  }
}
```



