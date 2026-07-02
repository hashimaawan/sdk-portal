# List of TXT Validation Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3QlMjUyMG9mJTI1MjBUWFQlMjUyMHZhbGlkYXRpb24lMjUyMHJlY29yZA

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`ListOfTxtValidationRecord`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `TxtName` | `string` | Optional, Read-only | - |
| `TxtValue` | `string` | Optional, Read-only | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

ListOfTxtValidationRecord listOfTxtValidationRecord = new ListOfTxtValidationRecord
{
    TxtName = "_acme-challenge.app.example.com",
    TxtValue = "lXLOcN6cPv0nproViNcUHcahD9TrIPlNgdwesj0pYpk",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



