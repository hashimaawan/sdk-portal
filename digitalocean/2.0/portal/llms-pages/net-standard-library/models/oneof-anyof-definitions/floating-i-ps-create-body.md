# Floating I Ps Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nSVBzQ3JlYXRlQm9keQ


# Class Name

`FloatingIPsCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`AssignToDroplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/assign-to-droplet.md) | FloatingIPsCreateBody.FromAssignToDroplet(AssignToDroplet assignToDroplet) |
| [`ReserveToRegion`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/reserve-to-region.md) | FloatingIPsCreateBody.FromReserveToRegion(ReserveToRegion reserveToRegion) |


# AssignToDroplet

## Initialization Code

### Example

```csharp
FloatingIPsCreateBody value = FloatingIPsCreateBody.FromAssignToDroplet(
    new AssignToDroplet
    {
        DropletId = 2457247,
    }
);
```


# ReserveToRegion

## Initialization Code

### Example

```csharp
FloatingIPsCreateBody value = FloatingIPsCreateBody.FromReserveToRegion(
    new ReserveToRegion
    {
        Region = "nyc3",
        ProjectId = new Guid("746c6152-2fa2-11ed-92d3-27aaa54e4988"),
    }
);
```



