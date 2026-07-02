# A Criterion for Routing HTTP Traffic to a Component

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkElMjUyMGNyaXRlcmlvbiUyNTIwZm9yJTI1MjByb3V0aW5nJTI1MjBIVFRQJTI1MjB0cmFmZmljJTI1MjB0byUyNTIwYSUyNTIwY29tcG9uZW50Lg

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`ACriterionForRoutingHttpTrafficToAComponent`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Path` | `string` | Optional | An HTTP path prefix. Paths must start with / and must be unique across all components within an app. |
| `PreservePathPrefix` | `bool?` | Optional | An optional flag to preserve the path that is forwarded to the backend service. By default, the HTTP request path will be trimmed from the left when forwarded to the component. For example, a component with `path=/api` will have requests to `/api/list` trimmed to `/list`. If this value is `true`, the path will remain `/api/list`. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

ACriterionForRoutingHttpTrafficToAComponent aCriterionForRoutingHttpTrafficToAComponent = new ACriterionForRoutingHttpTrafficToAComponent
{
    Path = "/api",
    PreservePathPrefix = true,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



