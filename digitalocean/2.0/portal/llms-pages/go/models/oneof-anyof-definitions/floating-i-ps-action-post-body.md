# Floating I Ps Action Post Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkZsb2F0aW5nSVBzQWN0aW9uUG9zdEJvZHk


# Class Name

`FloatingIPsActionPostBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.BaseTypeInterface`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/base-type.md) | models.FloatingIPsActionPostBodyContainer.FromBaseType(models.BaseTypeInterface baseType) |
| [`models.V2FloatingIpsActionsRequestInterface`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-floating-ips-actions-request.md) | models.FloatingIPsActionPostBodyContainer.FromV2FloatingIpsActionsRequest(models.V2FloatingIpsActionsRequestInterface v2FloatingIpsActionsRequest) |


# models.BaseTypeInterface

## Initialization Code

### Example

```go
value := models.FloatingIPsActionPostBodyContainer.FromBaseType(models.BaseTypeInterface(&models.BaseTypeInterface(&models.BaseType{
    Type:                  models.ToPointer("BaseType"),
})))
```


# models.V2FloatingIpsActionsRequestInterface

## Initialization Code

### Example

```go
value := models.FloatingIPsActionPostBodyContainer.FromV2FloatingIpsActionsRequest(models.V2FloatingIpsActionsRequestInterface(&models.V2FloatingIpsActionsRequest{
    BaseType:  models.BaseType{
        Type:                  models.ToPointer("V2 Floating Ips Actions Request"),
    },
    DropletId: 758604968,
}))
```



