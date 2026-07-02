# Type 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlR5cGUx

- DEFAULT: The default `.ondigitalocean.app` domain assigned to this app
- PRIMARY: The primary domain for this app that is displayed as the default in the control panel, used in bindable environment variables, and any other places that reference an app's live URL. Only one domain may be set as primary.
- ALIAS: A non-primary domain


# Enum Type Name

`Type1`


# Fields

| Name |
|  --- |
| `Unspecified` |
| `Default` |
| `Primary` |
| `Alias` |


# Example

```csharp
using DigitalOceanApi.Standard.Models;

Type1 type1 = Type1.Primary;
```



