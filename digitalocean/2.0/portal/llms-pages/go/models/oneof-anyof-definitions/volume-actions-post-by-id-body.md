# Volume Actions Post by Id Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlZvbHVtZUFjdGlvbnNQb3N0QnlJZEJvZHk


# Class Name

`VolumeActionsPostByIdBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.V2VolumesActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-volumes-actions-request.md) | models.VolumeActionsPostByIdBodyContainer.FromV2VolumesActionsRequest(models.V2VolumesActionsRequest v2VolumesActionsRequest) |
| [`models.V2VolumesActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-volumes-actions-request-1.md) | models.VolumeActionsPostByIdBodyContainer.FromV2VolumesActionsRequest1(models.V2VolumesActionsRequest1 v2VolumesActionsRequest1) |
| [`models.V2VolumesActionsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-volumes-actions-request-2.md) | models.VolumeActionsPostByIdBodyContainer.FromV2VolumesActionsRequest2(models.V2VolumesActionsRequest2 v2VolumesActionsRequest2) |


# models.V2VolumesActionsRequest

## Initialization Code

### Example

```go
value := models.VolumeActionsPostByIdBodyContainer.FromV2VolumesActionsRequest(models.V2VolumesActionsRequest{
    Region:                models.ToPointer(models.Region2_Nyc3),
    Type:                  models.Type21_Attach,
    DropletId:             11612190,
    Tags:                  models.NewOptional(models.ToPointer([]string{
        "base-image",
        "prod",
    })),
})
```


# models.V2VolumesActionsRequest1

## Initialization Code

### Example

```go
value := models.VolumeActionsPostByIdBodyContainer.FromV2VolumesActionsRequest1(models.V2VolumesActionsRequest1{
    Region:                models.ToPointer(models.Region2_Nyc3),
    Type:                  models.Type21_Attach,
    DropletId:             11612190,
})
```


# models.V2VolumesActionsRequest2

## Initialization Code

### Example

```go
value := models.VolumeActionsPostByIdBodyContainer.FromV2VolumesActionsRequest2(models.V2VolumesActionsRequest2{
    Region:                models.ToPointer(models.Region2_Nyc3),
    Type:                  models.Type21_Attach,
    SizeGigabytes:         15384,
})
```



