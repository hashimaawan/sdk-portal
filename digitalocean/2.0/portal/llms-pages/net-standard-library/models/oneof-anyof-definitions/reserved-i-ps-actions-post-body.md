# Reserved I Ps Actions Post Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc2VydmVkSVBzQWN0aW9uc1Bvc3RCb2R5


# Class Name

`ReservedIPsActionsPostBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`BaseType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/base-type.md) | ReservedIPsActionsPostBody.FromBaseType(BaseType baseType) |
| [`V2ReservedIpsActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-reserved-ips-actions-request.md) | ReservedIPsActionsPostBody.FromV2ReservedIpsActionsRequest(V2ReservedIpsActionsRequest v2ReservedIpsActionsRequest) |


# BaseType

## Initialization Code

### Example

```csharp
ReservedIPsActionsPostBody value = ReservedIPsActionsPostBody.FromBaseType(
    new BaseType
    {
        Type = "BaseType",
    }
);
```


# V2ReservedIpsActionsRequest

## Initialization Code

### Example

```csharp
ReservedIPsActionsPostBody value = ReservedIPsActionsPostBody.FromV2ReservedIpsActionsRequest(
    new V2ReservedIpsActionsRequest
    {
        DropletId = 758604968,
        Type = "V2 Reserved Ips Actions Request",
    }
);
```



