# Invoice Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkludm9pY2VJdGVt

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`InvoiceItem`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Amount` | `string` | Optional | Billed amount of this invoice item. Billed in USD. |
| `Description` | `string` | Optional | Description of the invoice item. |
| `Duration` | `string` | Optional | Duration of time this invoice item was used and subsequently billed. |
| `DurationUnit` | `string` | Optional | Unit of time for duration. |
| `EndTime` | `string` | Optional | Time the invoice item stopped being billed for usage. |
| `GroupDescription` | `string` | Optional | Description of the invoice item when it is a grouped set of usage, such  as DOKS or databases. |
| `Product` | `string` | Optional | Name of the product being billed in the invoice item. |
| `ProjectName` | `string` | Optional | Name of the DigitalOcean Project this resource belongs to. |
| `ResourceId` | `string` | Optional | ID of the resource billing in the invoice item if available. |
| `ResourceUuid` | `string` | Optional | UUID of the resource billing in the invoice item if available. |
| `StartTime` | `string` | Optional | Time the invoice item began to be billed for usage. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

InvoiceItem invoiceItem = new InvoiceItem
{
    Amount = "12.34",
    Description = "a56e086a317d8410c8b4cfd1f4dc9f82",
    Duration = "744",
    DurationUnit = "Hours",
    EndTime = "2020-02-01T00:00:00Z",
    GroupDescription = "my-doks-cluster",
    Product = "Kubernetes Clusters",
    ProjectName = "web",
    ResourceId = "2353624",
    ResourceUuid = "711157cb-37c8-4817-b371-44fa3504a39c",
    StartTime = "2020-01-01T00:00:00Z",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



