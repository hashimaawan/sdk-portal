# Reserved I Ps Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc2VydmVkSVBzQ3JlYXRlQm9keQ


# Class Name

`ReservedIPsCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`AssignToDroplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/assign-to-droplet-1.md) | ReservedIPsCreateBody.FromAssignToDroplet1(AssignToDroplet1 assignToDroplet1) |
| [`ReserveToRegion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/reserve-to-region-1.md) | ReservedIPsCreateBody.FromReserveToRegion1(ReserveToRegion1 reserveToRegion1) |


# AssignToDroplet1

## Initialization Code

### Example

```csharp
ReservedIPsCreateBody value = ReservedIPsCreateBody.FromAssignToDroplet1(
    new AssignToDroplet1
    {
        DropletId = 2457247,
    }
);
```


# ReserveToRegion1

## Initialization Code

### Example

```csharp
ReservedIPsCreateBody value = ReservedIPsCreateBody.FromReserveToRegion1(
    new ReserveToRegion1
    {
        Region = "nyc3",
        ProjectId = new Guid("746c6152-2fa2-11ed-92d3-27aaa54e4988"),
    }
);
```



