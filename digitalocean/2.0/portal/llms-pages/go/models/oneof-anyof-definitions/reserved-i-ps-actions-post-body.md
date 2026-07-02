# Reserved I Ps Actions Post Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlc2VydmVkSVBzQWN0aW9uc1Bvc3RCb2R5


# Class Name

`ReservedIPsActionsPostBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.BaseTypeInterface`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/base-type.md) | models.ReservedIPsActionsPostBodyContainer.FromBaseType(models.BaseTypeInterface baseType) |
| [`models.V2ReservedIpsActionsRequestInterface`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-reserved-ips-actions-request.md) | models.ReservedIPsActionsPostBodyContainer.FromV2ReservedIpsActionsRequest(models.V2ReservedIpsActionsRequestInterface v2ReservedIpsActionsRequest) |


# models.BaseTypeInterface

## Initialization Code

### Example

```go
value := models.ReservedIPsActionsPostBodyContainer.FromBaseType(models.BaseTypeInterface(&models.BaseTypeInterface(&models.BaseType{
    Type:                  models.ToPointer("BaseType"),
})))
```


# models.V2ReservedIpsActionsRequestInterface

## Initialization Code

### Example

```go
value := models.ReservedIPsActionsPostBodyContainer.FromV2ReservedIpsActionsRequest(models.V2ReservedIpsActionsRequestInterface(&models.V2ReservedIpsActionsRequest{
    BaseType:  models.BaseType{
        Type:                  models.ToPointer("V2 Reserved Ips Actions Request"),
    },
    DropletId: 758604968,
}))
```



