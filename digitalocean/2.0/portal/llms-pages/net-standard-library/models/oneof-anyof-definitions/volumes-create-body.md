# Volumes Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlZvbHVtZXNDcmVhdGVCb2R5


# Class Name

`VolumesCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`V2VolumesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-volumes-request.md) | VolumesCreateBody.FromV2VolumesRequest(V2VolumesRequest v2VolumesRequest) |
| [`V2VolumesRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-volumes-request-1.md) | VolumesCreateBody.FromV2VolumesRequest1(V2VolumesRequest1 v2VolumesRequest1) |


# V2VolumesRequest

## Initialization Code

### Example

```csharp
VolumesCreateBody value = VolumesCreateBody.FromV2VolumesRequest(
    new V2VolumesRequest
    {
        Name = "example",
        SizeGigabytes = 10,
        Region = Region2.Nyc3,
        CreatedAt = "2020-03-02T17:00:49Z",
        Description = "Block store for examples",
        DropletIds = new List<int>
        {

        },
        Id = "506f78a4-e098-11e5-ad9f-000f53306ae1",
        Tags = new List<string>
        {
            "base-image",
            "prod",
        },
        SnapshotId = "b0798135-fb76-11eb-946a-0a58ac146f33",
        FilesystemType = "ext4",
    }
);
```


# V2VolumesRequest1

## Initialization Code

### Example

```csharp
VolumesCreateBody value = VolumesCreateBody.FromV2VolumesRequest1(
    new V2VolumesRequest1
    {
        Name = "example",
        SizeGigabytes = 10,
        Region = Region2.Nyc3,
        CreatedAt = "2020-03-02T17:00:49Z",
        Description = "Block store for examples",
        DropletIds = new List<int>
        {

        },
        Id = "506f78a4-e098-11e5-ad9f-000f53306ae1",
        Tags = new List<string>
        {
            "base-image",
            "prod",
        },
        SnapshotId = "b0798135-fb76-11eb-946a-0a58ac146f33",
        FilesystemType = "ext4",
    }
);
```



