# Cors

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNvcnM

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Cors`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AllowCredentials` | `bool?` | Optional | Whether browsers should expose the response to the client-side JavaScript code when the request’s credentials mode is include. This configures the `Access-Control-Allow-Credentials` header. |
| `AllowHeaders` | `List<string>` | Optional | The set of allowed HTTP request headers. This configures the `Access-Control-Allow-Headers` header. |
| `AllowMethods` | `List<string>` | Optional | The set of allowed HTTP methods. This configures the `Access-Control-Allow-Methods` header. |
| `AllowOrigins` | [`List<AllowOrigin>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/allow-origin.md) | Optional | The set of allowed CORS origins. |
| `ExposeHeaders` | `List<string>` | Optional | The set of HTTP response headers that browsers are allowed to access. This configures the `Access-Control-Expose-Headers` header. |
| `MaxAge` | `string` | Optional | An optional duration specifying how long browsers can cache the results of a preflight request. This configures the `Access-Control-Max-Age` header. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Cors cors = new Cors
{
    AllowCredentials = false,
    AllowHeaders = new List<string>
    {
        "Content-Type",
        "X-Custom-Header",
    },
    AllowMethods = new List<string>
    {
        "GET",
        "OPTIONS",
        "POST",
        "PUT",
        "PATCH",
        "DELETE",
    },
    AllowOrigins = new List<AllowOrigin>
    {
        new AllowOrigin
        {
            Exact = "https://www.example.com",
            Prefix = "prefix6",
            Regex = "regex4",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new AllowOrigin
        {
            Exact = "exact8",
            Prefix = "prefix6",
            Regex = "^.*example.com",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ExposeHeaders = new List<string>
    {
        "Content-Encoding",
        "X-Custom-Header",
    },
    MaxAge = "5h30m",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



