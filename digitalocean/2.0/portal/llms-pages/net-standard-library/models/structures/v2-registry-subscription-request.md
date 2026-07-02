# V2 Registry Subscription Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwU3Vic2NyaXB0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2RegistrySubscriptionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `TierSlug` | [`TierSlug?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/tier-slug.md) | Optional | The slug of the subscription tier to sign up for. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

V2RegistrySubscriptionRequest v2RegistrySubscriptionRequest = new V2RegistrySubscriptionRequest
{
    TierSlug = TierSlug.Basic,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



