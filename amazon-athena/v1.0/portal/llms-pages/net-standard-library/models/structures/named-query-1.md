# Named Query 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk5hbWVkUXVlcnkx

*This model accepts additional fields of type object.*


# Class Name

`NamedQuery1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Description` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `Database` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `QueryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `NamedQueryId` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `WorkGroup` | `string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

NamedQuery1 namedQuery1 = new NamedQuery1
{
    Name = "Name0",
    Database = "Database8",
    QueryString = "QueryString2",
    Description = "Description6",
    NamedQueryId = "NamedQueryId2",
    WorkGroup = "WorkGroup2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



