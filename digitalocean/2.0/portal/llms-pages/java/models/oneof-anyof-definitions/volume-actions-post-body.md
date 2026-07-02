# Volume Actions Post Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlZvbHVtZUFjdGlvbnNQb3N0Qm9keQ


# Class Name

`VolumeActionsPostBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`V2VolumesActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-volumes-actions-request.md) | VolumeActionsPostBody.fromV2VolumesActionsRequest(V2VolumesActionsRequest v2VolumesActionsRequest) |
| [`V2VolumesActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-volumes-actions-request-1.md) | VolumeActionsPostBody.fromV2VolumesActionsRequest1(V2VolumesActionsRequest1 v2VolumesActionsRequest1) |


# V2VolumesActionsRequest

## Initialization Code

### Example

```java
VolumeActionsPostBody.fromV2VolumesActionsRequest(
        new V2VolumesActionsRequest.Builder(
            Type21.ATTACH,
            11612190
        )
        .region(Region2.NYC3)
        .tags(Arrays.asList(
                "base-image",
                "prod"
            ))
        .build()
    )
```


# V2VolumesActionsRequest1

## Initialization Code

### Example

```java
VolumeActionsPostBody.fromV2VolumesActionsRequest1(
        new V2VolumesActionsRequest1.Builder(
            Type21.ATTACH,
            11612190
        )
        .region(Region2.NYC3)
        .build()
    )
```



