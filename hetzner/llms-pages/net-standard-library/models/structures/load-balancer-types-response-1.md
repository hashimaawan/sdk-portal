# Load Balancer Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2Ux


# Class Name

`LoadBalancerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancerType` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/load-balancer-type.md) | Optional | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

LoadBalancerTypesResponse1 loadBalancerTypesResponse1 = new LoadBalancerTypesResponse1
{
    LoadBalancerType = new LoadBalancerType
    {
        Deprecated = "deprecated2",
        Description = "description4",
        Id = 205.06,
        MaxAssignedCertificates = 211.64,
        MaxConnections = 136.32,
        MaxServices = 199.18,
        MaxTargets = 152.52,
        Name = "name6",
        Prices = new List<Price>
        {
            new Price
            {
                Location = "location8",
                PriceHourly = new PriceHourly
                {
                    Gross = "gross4",
                    Net = "net2",
                },
                PriceMonthly = new PriceMonthly
                {
                    Gross = "gross2",
                    Net = "net0",
                },
            },
            new Price
            {
                Location = "location8",
                PriceHourly = new PriceHourly
                {
                    Gross = "gross4",
                    Net = "net2",
                },
                PriceMonthly = new PriceMonthly
                {
                    Gross = "gross2",
                    Net = "net0",
                },
            },
            new Price
            {
                Location = "location8",
                PriceHourly = new PriceHourly
                {
                    Gross = "gross4",
                    Net = "net2",
                },
                PriceMonthly = new PriceMonthly
                {
                    Gross = "gross2",
                    Net = "net0",
                },
            },
        },
    },
};
```



