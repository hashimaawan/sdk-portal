# Floating I Ps Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkZsb2F0aW5nSVBzQ3JlYXRlQm9keQ


# Class Name

`FloatingIPsCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`AssignToDroplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/assign-to-droplet.md) | FloatingIPsCreateBody.fromAssignToDroplet(AssignToDroplet assignToDroplet) |
| [`ReserveToRegion`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/reserve-to-region.md) | FloatingIPsCreateBody.fromReserveToRegion(ReserveToRegion reserveToRegion) |


# AssignToDroplet

## Initialization Code

### Example

```java
FloatingIPsCreateBody.fromAssignToDroplet(
        new AssignToDroplet.Builder(
            2457247
        )
        .build()
    )
```


# ReserveToRegion

## Initialization Code

### Example

```java
FloatingIPsCreateBody.fromReserveToRegion(
        new ReserveToRegion.Builder(
            "nyc3"
        )
        .projectId(UUID.fromString("746c6152-2fa2-11ed-92d3-27aaa54e4988"))
        .build()
    )
```



