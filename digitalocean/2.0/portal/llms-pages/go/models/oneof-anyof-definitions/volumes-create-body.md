# Volumes Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlZvbHVtZXNDcmVhdGVCb2R5


# Class Name

`VolumesCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.V2VolumesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-volumes-request.md) | models.VolumesCreateBodyContainer.FromV2VolumesRequest(models.V2VolumesRequest v2VolumesRequest) |
| [`models.V2VolumesRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-volumes-request-1.md) | models.VolumesCreateBodyContainer.FromV2VolumesRequest1(models.V2VolumesRequest1 v2VolumesRequest1) |


# models.V2VolumesRequest

## Initialization Code

### Example

```go
value := models.VolumesCreateBodyContainer.FromV2VolumesRequest(models.V2VolumesRequest{
    CreatedAt:             models.ToPointer("2020-03-02T17:00:49Z"),
    Description:           models.ToPointer("Block store for examples"),
    DropletIds:            models.NewOptional(models.ToPointer([]int{
    })),
    Id:                    models.ToPointer("506f78a4-e098-11e5-ad9f-000f53306ae1"),
    Name:                  "example",
    SizeGigabytes:         10,
    Tags:                  models.NewOptional(models.ToPointer([]string{
        "base-image",
        "prod",
    })),
    SnapshotId:            models.ToPointer("b0798135-fb76-11eb-946a-0a58ac146f33"),
    FilesystemType:        models.ToPointer("ext4"),
    Region:                models.Region2_Nyc3,
})
```


# models.V2VolumesRequest1

## Initialization Code

### Example

```go
value := models.VolumesCreateBodyContainer.FromV2VolumesRequest1(models.V2VolumesRequest1{
    CreatedAt:             models.ToPointer("2020-03-02T17:00:49Z"),
    Description:           models.ToPointer("Block store for examples"),
    DropletIds:            models.NewOptional(models.ToPointer([]int{
    })),
    Id:                    models.ToPointer("506f78a4-e098-11e5-ad9f-000f53306ae1"),
    Name:                  "example",
    SizeGigabytes:         10,
    Tags:                  models.NewOptional(models.ToPointer([]string{
        "base-image",
        "prod",
    })),
    SnapshotId:            models.ToPointer("b0798135-fb76-11eb-946a-0a58ac146f33"),
    FilesystemType:        models.ToPointer("ext4"),
    Region:                models.Region2_Nyc3,
})
```



