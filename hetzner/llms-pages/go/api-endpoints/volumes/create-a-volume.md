# Create a Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZDcmVhdGUlMjUyMGElMjUyMFZvbHVtZQ

Creates a new Volume attached to a Server. If you want to create a Volume that is not attached to a Server, you need to provide the `location` key instead of `server`. This can be either the ID or the name of the Location this Volume will be created in. Note that a Volume can be attached to a Server only in the same Location as the Volume itself.

Specifying the Server during Volume creation will automatically attach the Volume to that Server after it has been initialized. In that case, the `next_actions` key in the response is an array which contains a single `attach_volume` action.

The minimum Volume size is 10GB and the maximum size is 10TB (10240GB).

A volume’s name can consist of alphanumeric characters, dashes, underscores, and dots, but has to start and end with an alphanumeric character. The total length is limited to 64 characters. Volume names must be unique per Project.

#### Call specific error codes

| Code                                | Description                                         |
|-------------------------------------|-----------------------------------------------------|
| `no_space_left_in_location`         | There is no volume space left in the given location |

:information_source: **Note** This endpoint does not require authentication.

```go
CreateAVolume(
    ctx context.Context,
    body *models.CreateVolumeRequest) (
    models.ApiResponse[models.VolumesResponse1],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`*models.CreateVolumeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/create-volume-request.md) | Body, Optional | - |


# Response Type

**201**: The `volume` key contains the Volume that was just created

The `action` key contains the Action tracking Volume creation

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.VolumesResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/volumes-response-1.md).


# Example Usage

```go
ctx := context.Background()

body := models.CreateVolumeRequest{
    Automount:            models.ToPointer(false),
    Format:               models.ToPointer("xfs"),
    Labels:               models.ToPointer(interface{}("[labelkey, value]")),
    Location:             models.ToPointer("nbg1"),
    Name:                 "test-database",
    Size:                 42,
}

apiResponse, err := volumesController.CreateAVolume(ctx, &body)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "create_volume",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 42,
        "type": "server"
      },
      {
        "id": 554,
        "type": "volume"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  },
  "next_actions": [
    {
      "command": "attach_volume",
      "error": {
        "code": "action_failed",
        "message": "Action failed"
      },
      "finished": null,
      "id": 13,
      "progress": 0,
      "resources": [
        {
          "id": 42,
          "type": "server"
        },
        {
          "id": 554,
          "type": "volume"
        }
      ],
      "started": "2016-01-30T23:50:00+00:00",
      "status": "running"
    }
  ],
  "volume": {
    "created": "2016-01-30T23:50:11+00:00",
    "format": "xfs",
    "id": 4711,
    "labels": {
      "env": "dev"
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



