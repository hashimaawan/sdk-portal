# Query Execution Context

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dA

The database and data catalog context in which the query execution occurs.


# Class Name

`QueryExecutionContext`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Database` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `Catalog` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |


# Example

```csharp
using AmazonAthena.Standard.Models;

QueryExecutionContext queryExecutionContext = new QueryExecutionContext
{
    Database = "Database0",
    Catalog = "Catalog6",
};
```



