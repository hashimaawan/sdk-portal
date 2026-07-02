# User Billing Address

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVzZXJCaWxsaW5nQWRkcmVzcw

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`UserBillingAddress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddressLine1` | `string` | Optional | Street address line 1 |
| `AddressLine2` | `string` | Optional | Street address line 2 |
| `City` | `string` | Optional | City |
| `CountryIso2Code` | `string` | Optional | Country (ISO2) code |
| `CreatedAt` | `string` | Optional | Timestamp billing address was created |
| `PostalCode` | `string` | Optional | Postal code |
| `Region` | `string` | Optional | Region |
| `UpdatedAt` | `string` | Optional | Timestamp billing address was updated |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

UserBillingAddress userBillingAddress = new UserBillingAddress
{
    AddressLine1 = "101 Shark Row",
    AddressLine2 = "address_line24",
    City = "Atlantis",
    CountryIso2Code = "US",
    CreatedAt = "2019-09-03T16:34:46.000+00:00",
    PostalCode = "12345",
    Region = "OC",
    UpdatedAt = "2019-09-03T16:34:46.000+00:00",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



