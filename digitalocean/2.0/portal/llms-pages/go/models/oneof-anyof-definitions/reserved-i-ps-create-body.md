# Reserved I Ps Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlc2VydmVkSVBzQ3JlYXRlQm9keQ


# Class Name

`ReservedIPsCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.AssignToDroplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/assign-to-droplet-1.md) | models.ReservedIPsCreateBodyContainer.FromAssignToDroplet1(models.AssignToDroplet1 assignToDroplet1) |
| [`models.ReserveToRegion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/reserve-to-region-1.md) | models.ReservedIPsCreateBodyContainer.FromReserveToRegion1(models.ReserveToRegion1 reserveToRegion1) |


# models.AssignToDroplet1

## Initialization Code

### Example

```go
value := models.ReservedIPsCreateBodyContainer.FromAssignToDroplet1(models.AssignToDroplet1{
    DropletId:             2457247,
})
```


# models.ReserveToRegion1

## Initialization Code

### Example

```go
value := models.ReservedIPsCreateBodyContainer.FromReserveToRegion1(models.ReserveToRegion1{
    ProjectId:             models.ToPointer(uuid.MustParse("746c6152-2fa2-11ed-92d3-27aaa54e4988")),
    Region:                "nyc3",
})
```



