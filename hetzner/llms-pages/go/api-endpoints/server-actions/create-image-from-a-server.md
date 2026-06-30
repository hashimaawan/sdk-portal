# Create Image from a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkNyZWF0ZSUyNTIwSW1hZ2UlMjUyMGZyb20lMjUyMGElMjUyMFNlcnZlcg

Creates an Image (snapshot) from a Server by copying the contents of its disks. This creates a snapshot of the current state of the disk and copies it into an Image. If the Server is currently running you must make sure that its disk content is consistent. Otherwise, the created Image may not be readable.

To make sure disk content is consistent, we recommend to shut down the Server prior to creating an Image.

You can either create a `backup` Image that is bound to the Server and therefore will be deleted when the Server is deleted, or you can create an `snapshot` Image which is completely independent of the Server it was created from and will survive Server deletion. Backup Images are only available when the backup option is enabled for the Server. Snapshot Images are billed on a per GB basis.

:information_source: **Note** This endpoint does not require authentication.

```go
CreateImageFromAServer(
    ctx context.Context,
    id int,
    body *models.CreateImageRequest) (
    models.ApiResponse[models.ServersActionsCreateImageResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`*models.CreateImageRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/create-image-request.md) | Body, Optional | - |


# Response Type

**201**: The `image` key in the reply contains an the created Image, which is an object with this structure

The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ServersActionsCreateImageResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/servers-actions-create-image-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.CreateImageRequest{
    Description:          models.ToPointer("my image"),
    Type:                 models.ToPointer(models.Type63Enum_SNAPSHOT),
}

apiResponse, err := serverActionsController.CreateImageFromAServer(ctx, id, &body)
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
    "command": "create_image",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": "2016-01-30T23:56:00+00:00",
    "id": 13,
    "progress": 100,
    "resources": [
      {
        "id": 42,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  },
  "image": {
    "bound_to": null,
    "created": "2016-01-30T23:50:00+00:00",
    "created_from": {
      "id": 1,
      "name": "Server"
    },
    "deleted": null,
    "deprecated": "2018-02-28T00:00:00+00:00",
    "description": "my image",
    "disk_size": 10,
    "id": 4711,
    "image_size": 2.3,
    "labels": {
      "env": "dev"
    },
    "name": null,
    "os_flavor": "ubuntu",
    "os_version": "20.04",
    "protection": {
      "delete": false
    },
    "rapid_deploy": false,
    "status": "creating",
    "type": "snapshot"
  }
}
```



