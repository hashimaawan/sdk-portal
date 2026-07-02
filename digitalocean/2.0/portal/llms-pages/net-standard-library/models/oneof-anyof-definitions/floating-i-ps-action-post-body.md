# Floating I Ps Action Post Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nSVBzQWN0aW9uUG9zdEJvZHk


# Class Name

`FloatingIPsActionPostBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`BaseType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/base-type.md) | FloatingIPsActionPostBody.FromBaseType(BaseType baseType) |
| [`V2FloatingIpsActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-floating-ips-actions-request.md) | FloatingIPsActionPostBody.FromV2FloatingIpsActionsRequest(V2FloatingIpsActionsRequest v2FloatingIpsActionsRequest) |


# BaseType

## Initialization Code

### Example

```csharp
FloatingIPsActionPostBody value = FloatingIPsActionPostBody.FromBaseType(
    new BaseType
    {
        Type = "BaseType",
    }
);
```


# V2FloatingIpsActionsRequest

## Initialization Code

### Example

```csharp
FloatingIPsActionPostBody value = FloatingIPsActionPostBody.FromV2FloatingIpsActionsRequest(
    new V2FloatingIpsActionsRequest
    {
        DropletId = 758604968,
        Type = "V2 Floating Ips Actions Request",
    }
);
```



