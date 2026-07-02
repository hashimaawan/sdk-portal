# List Databases Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNPdXRwdXQ


# Class Name

`ListDatabasesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DatabaseList` | [`List<Database>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/database.md) | Optional | - |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

ListDatabasesOutput listDatabasesOutput = new ListDatabasesOutput
{
    DatabaseList = new List<Database>
    {
        new Database
        {
            Name = "Name4",
            Description = "Description8",
            Parameters = new Parameters
            {
            },
        },
        new Database
        {
            Name = "Name4",
            Description = "Description8",
            Parameters = new Parameters
            {
            },
        },
        new Database
        {
            Name = "Name4",
            Description = "Description8",
            Parameters = new Parameters
            {
            },
        },
    },
    NextToken = "NextToken6",
};
```



