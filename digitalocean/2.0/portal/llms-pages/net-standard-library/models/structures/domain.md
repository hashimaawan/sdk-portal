# Domain

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRvbWFpbg

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Domain`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Domain` | `string` | Required | The hostname for the domain<br><br>**Constraints**: *Minimum Length*: `4`, *Maximum Length*: `253`, *Pattern*: `^((xn--)?[a-zA-Z0-9]+(-[a-zA-Z0-9]+)*\.)+[a-zA-Z]{2,}\.?$` |
| `MinimumTlsVersion` | [`MinimumTlsVersion?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/minimum-tls-version.md) | Optional | The minimum version of TLS a client application can use to access resources for the domain.  Must be one of the following values wrapped within quotations: `"1.2"` or `"1.3"`.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `3` |
| `Type` | [`Type1?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/type-1.md) | Optional | - DEFAULT: The default `.ondigitalocean.app` domain assigned to this app<br>- PRIMARY: The primary domain for this app that is displayed as the default in the control panel, used in bindable environment variables, and any other places that reference an app's live URL. Only one domain may be set as primary.<br>- ALIAS: A non-primary domain<br><br>**Default**: `Type1.UNSPECIFIED` |
| `Wildcard` | `bool?` | Optional | Indicates whether the domain includes all sub-domains, in addition to the given domain |
| `Zone` | `string` | Optional | Optional. If the domain uses DigitalOcean DNS and you would like App<br>Platform to automatically manage it for you, set this to the name of the<br>domain on your account.<br><br>For example, If the domain you are adding is `app.domain.com`, the zone<br>could be `domain.com`. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Domain domain = new Domain
{
    DomainProp = "app.example.com",
    MinimumTlsVersion = MinimumTlsVersion.Enum13,
    Type = Type1.Default,
    Wildcard = true,
    Zone = "example.com",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



