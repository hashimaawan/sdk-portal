# Volumes Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlZvbHVtZXNDcmVhdGVCb2R5


# Class Name

`VolumesCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`V2VolumesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-volumes-request.md) | VolumesCreateBody.fromV2VolumesRequest(V2VolumesRequest v2VolumesRequest) |
| [`V2VolumesRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-volumes-request-1.md) | VolumesCreateBody.fromV2VolumesRequest1(V2VolumesRequest1 v2VolumesRequest1) |


# V2VolumesRequest

## Initialization Code

### Example

```java
VolumesCreateBody.fromV2VolumesRequest(
        new V2VolumesRequest.Builder(
            "example",
            10,
            Region2.NYC3
        )
        .createdAt("2020-03-02T17:00:49Z")
        .description("Block store for examples")
        .dropletIds(Arrays.asList(

            ))
        .id("506f78a4-e098-11e5-ad9f-000f53306ae1")
        .tags(Arrays.asList(
                "base-image",
                "prod"
            ))
        .snapshotId("b0798135-fb76-11eb-946a-0a58ac146f33")
        .filesystemType("ext4")
        .build()
    )
```


# V2VolumesRequest1

## Initialization Code

### Example

```java
VolumesCreateBody.fromV2VolumesRequest1(
        new V2VolumesRequest1.Builder(
            "example",
            10,
            Region2.NYC3
        )
        .createdAt("2020-03-02T17:00:49Z")
        .description("Block store for examples")
        .dropletIds(Arrays.asList(

            ))
        .id("506f78a4-e098-11e5-ad9f-000f53306ae1")
        .tags(Arrays.asList(
                "base-image",
                "prod"
            ))
        .snapshotId("b0798135-fb76-11eb-946a-0a58ac146f33")
        .filesystemType("ext4")
        .build()
    )
```



