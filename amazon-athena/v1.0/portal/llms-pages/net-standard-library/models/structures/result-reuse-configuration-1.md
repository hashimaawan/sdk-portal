# Result Reuse Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQ29uZmlndXJhdGlvbjE


# Class Name

`ResultReuseConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResultReuseByAgeConfiguration` | [`ResultReuseByAgeConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/result-reuse-by-age-configuration-2.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

ResultReuseConfiguration1 resultReuseConfiguration1 = new ResultReuseConfiguration1
{
    ResultReuseByAgeConfiguration = new ResultReuseByAgeConfiguration2
    {
        Enabled = false,
        MaxAgeInMinutes = 26,
    },
};
```



