# Reserved I Ps Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlc2VydmVkSVBzQ3JlYXRlQm9keQ


# Class Name

`ReservedIPsCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`AssignToDroplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/assign-to-droplet-1.md) | ReservedIPsCreateBody.fromAssignToDroplet1(AssignToDroplet1 assignToDroplet1) |
| [`ReserveToRegion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/reserve-to-region-1.md) | ReservedIPsCreateBody.fromReserveToRegion1(ReserveToRegion1 reserveToRegion1) |


# AssignToDroplet1

## Initialization Code

### Example

```java
ReservedIPsCreateBody.fromAssignToDroplet1(
        new AssignToDroplet1.Builder(
            2457247
        )
        .build()
    )
```


# ReserveToRegion1

## Initialization Code

### Example

```java
ReservedIPsCreateBody.fromReserveToRegion1(
        new ReserveToRegion1.Builder(
            "nyc3"
        )
        .projectId(UUID.fromString("746c6152-2fa2-11ed-92d3-27aaa54e4988"))
        .build()
    )
```



