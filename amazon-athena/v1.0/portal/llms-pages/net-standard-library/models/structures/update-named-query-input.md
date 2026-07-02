# Update Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVwZGF0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type object.*


# Class Name

`UpdateNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQueryId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Description` | `string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `QueryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

UpdateNamedQueryInput updateNamedQueryInput = new UpdateNamedQueryInput
{
    NamedQueryId = "NamedQueryId8",
    Name = "Name4",
    QueryString = "QueryString6",
    Description = "Description2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



