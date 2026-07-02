# Column

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNvbHVtbg

Contains metadata for a column in a table.


# Class Name

`Column`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Type` | `string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096` |
| `Comment` | `string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `255` |


# Example

```csharp
using AmazonAthena.Standard.Models;

Column column = new Column
{
    Name = "Name6",
    Type = "Type6",
    Comment = "Comment2",
};
```



