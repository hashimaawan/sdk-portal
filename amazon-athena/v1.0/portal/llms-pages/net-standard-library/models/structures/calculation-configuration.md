# Calculation Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uQ29uZmlndXJhdGlvbg

Contains configuration information for the calculation.


# Class Name

`CalculationConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CodeBlock` | `string` | Optional | **Constraints**: *Maximum Length*: `68000` |


# Example

```csharp
using AmazonAthena.Standard.Models;

CalculationConfiguration calculationConfiguration = new CalculationConfiguration
{
    CodeBlock = "CodeBlock2",
};
```



