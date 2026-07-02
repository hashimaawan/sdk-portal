# List Work Groups Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzSW5wdXQ


# Class Name

`ListWorkGroupsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 1`, `<= 50` |


# Example

```csharp
using AmazonAthena.Standard.Models;

ListWorkGroupsInput listWorkGroupsInput = new ListWorkGroupsInput
{
    NextToken = "NextToken8",
    MaxResults = 50,
};
```



