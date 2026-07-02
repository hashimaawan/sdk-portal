# Datum

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRhdHVt

A piece of data (a field in the table).

*This model accepts additional fields of type object.*


# Class Name

`Datum`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `VarCharValue` | `string` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

Datum datum = new Datum
{
    VarCharValue = "VarCharValue8",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



