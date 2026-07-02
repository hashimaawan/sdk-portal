# Calculation Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uQ29uZmlndXJhdGlvbg

Contains configuration information for the calculation.

*This model accepts additional fields of type object.*


# Class Name

`CalculationConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CodeBlock` | `string` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

CalculationConfiguration calculationConfiguration = new CalculationConfiguration
{
    CodeBlock = "CodeBlock2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



