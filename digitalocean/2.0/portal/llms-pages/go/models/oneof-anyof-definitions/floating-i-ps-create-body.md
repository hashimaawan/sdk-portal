# Floating I Ps Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkZsb2F0aW5nSVBzQ3JlYXRlQm9keQ


# Class Name

`FloatingIPsCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.AssignToDroplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/assign-to-droplet.md) | models.FloatingIPsCreateBodyContainer.FromAssignToDroplet(models.AssignToDroplet assignToDroplet) |
| [`models.ReserveToRegion`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/reserve-to-region.md) | models.FloatingIPsCreateBodyContainer.FromReserveToRegion(models.ReserveToRegion reserveToRegion) |


# models.AssignToDroplet

## Initialization Code

### Example

```go
value := models.FloatingIPsCreateBodyContainer.FromAssignToDroplet(models.AssignToDroplet{
    DropletId:             2457247,
})
```


# models.ReserveToRegion

## Initialization Code

### Example

```go
value := models.FloatingIPsCreateBodyContainer.FromReserveToRegion(models.ReserveToRegion{
    ProjectId:             models.ToPointer(uuid.MustParse("746c6152-2fa2-11ed-92d3-27aaa54e4988")),
    Region:                "nyc3",
})
```



