# Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU

*This model accepts additional fields of type object.*


# Class Name

`LoadBalancerType`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Deprecated` | `string` | Required | Point in time when the Load Balancer type is deprecated (in ISO-8601 format) |
| `Description` | `string` | Required | Description of the Load Balancer type |
| `Id` | `double` | Required | ID of the Load Balancer type |
| `MaxAssignedCertificates` | `double` | Required | Number of SSL Certificates that can be assigned to a single Load Balancer |
| `MaxConnections` | `double` | Required | Number of maximum simultaneous open connections |
| `MaxServices` | `double` | Required | Number of services a Load Balancer of this type can have |
| `MaxTargets` | `double` | Required | Number of targets a single Load Balancer can have |
| `Name` | `string` | Required | Unique identifier of the Load Balancer type |
| `Prices` | [`List<Price>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/price.md) | Required | Prices in different network zones |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

LoadBalancerType loadBalancerType = new LoadBalancerType
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
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            PriceMonthly = new PriceMonthly
            {
                Gross = "1.1900000000000000",
                Net = "1.0000000000",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



