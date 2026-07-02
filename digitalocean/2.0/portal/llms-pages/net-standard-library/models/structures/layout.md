# Layout

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxheW91dA

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Layout`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NumNodes` | `int?` | Optional | - |
| `Sizes` | `List<string>` | Optional, Read-only | An array of objects containing the slugs available with various node counts |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Layout layout = new Layout
{
    NumNodes = 1,
    Sizes = new List<string>
    {
        "db-s-1vcpu-1gb",
        "db-s-1vcpu-2gb",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



