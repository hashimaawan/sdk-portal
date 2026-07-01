# Update a Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZVcGRhdGUlMjUyMGElMjUyMFZvbHVtZQ

Updates the Volume properties.

Note that when updating labels, the volume’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<VolumesResponse2>> updateAVolumeAsync(
    final String id,
    final UpdateVolumeRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Template, Required | ID of the Volume to update |
| `body` | [`UpdateVolumeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/update-volume-request.md) | Body, Optional | - |


# Response Type

**200**: The `volume` key contains the updated volume

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`VolumesResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/volumes-response-2.md).


# Example Usage

```java
String id = "id0";
UpdateVolumeRequest body = new UpdateVolumeRequest.Builder(
    "database-storage"
)
.build();

volumesApi.updateAVolumeAsync(id, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
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



