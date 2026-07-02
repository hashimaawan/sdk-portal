# Volume Actions Post by Id Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlZvbHVtZUFjdGlvbnNQb3N0QnlJZEJvZHk


# Class Name

`VolumeActionsPostByIdBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`V2VolumesActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-volumes-actions-request.md) | VolumeActionsPostByIdBody.FromV2VolumesActionsRequest(V2VolumesActionsRequest v2VolumesActionsRequest) |
| [`V2VolumesActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-volumes-actions-request-1.md) | VolumeActionsPostByIdBody.FromV2VolumesActionsRequest1(V2VolumesActionsRequest1 v2VolumesActionsRequest1) |
| [`V2VolumesActionsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-volumes-actions-request-2.md) | VolumeActionsPostByIdBody.FromV2VolumesActionsRequest2(V2VolumesActionsRequest2 v2VolumesActionsRequest2) |


# V2VolumesActionsRequest

## Initialization Code

### Example

```csharp
VolumeActionsPostByIdBody value = VolumeActionsPostByIdBody.FromV2VolumesActionsRequest(
    new V2VolumesActionsRequest
    {
        Type = Type21.Attach,
        DropletId = 11612190,
        Region = Region2.Nyc3,
        Tags = new List<string>
        {
            "base-image",
            "prod",
        },
    }
);
```


# V2VolumesActionsRequest1

## Initialization Code

### Example

```csharp
VolumeActionsPostByIdBody value = VolumeActionsPostByIdBody.FromV2VolumesActionsRequest1(
    new V2VolumesActionsRequest1
    {
        Type = Type21.Attach,
        DropletId = 11612190,
        Region = Region2.Nyc3,
    }
);
```


# V2VolumesActionsRequest2

## Initialization Code

### Example

```csharp
VolumeActionsPostByIdBody value = VolumeActionsPostByIdBody.FromV2VolumesActionsRequest2(
    new V2VolumesActionsRequest2
    {
        Type = Type21.Attach,
        SizeGigabytes = 15384,
        Region = Region2.Nyc3,
    }
);
```



