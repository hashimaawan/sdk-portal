# Load Balancer Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2U


# Class Name

`LoadBalancerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancerTypes` | [`List<LoadBalancerType>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-type.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

LoadBalancerTypesResponse loadBalancerTypesResponse = new LoadBalancerTypesResponse
{
    LoadBalancerTypes = new List<LoadBalancerType>
    {
        new LoadBalancerType
        {
            Deprecated = "2016-01-30T23:50:00+00:00",
            Description = "LB11",
            Id = 1,
            MaxAssignedCertificates = 10,
            MaxConnections = 20000,
            MaxServices = 5,
            MaxTargets = 25,
            Name = "lb11",
            Prices = new List<Price>
            {
                new Price
                {
                    Location = "fsn1",
                    PriceHourly = new PriceHourly
                    {
                        Gross = "1.1900000000000000",
                        Net = "1.0000000000",
                    },
                    PriceMonthly = new PriceMonthly
                    {
                        Gross = "1.1900000000000000",
                        Net = "1.0000000000",
                    },
                },
            },
        },
    },
};
```



