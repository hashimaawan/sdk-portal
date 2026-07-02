# Kernel

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRktlcm5lbA

**Note**: All Droplets created after March 2017 use internal kernels by default.
These Droplets will have this attribute set to `null`.

The current [kernel](https://www.digitalocean.com/docs/droplets/how-to/kernel/)
for Droplets with externally managed kernels. This will initially be set to
the kernel of the base image when the Droplet is created.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Kernel`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int?` | Optional | A unique number used to identify and reference a specific kernel. |
| `Name` | `string` | Optional | The display name of the kernel. This is shown in the web UI and is generally a descriptive title for the kernel in question. |
| `Version` | `string` | Optional | A standard kernel version string representing the version, patch, and release information. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Kernel kernel = new Kernel
{
    Id = 7515,
    Name = "DigitalOcean GrubLoader v0.2 (20160714)",
    Version = "2016.07.13-DigitalOcean_loader_Ubuntu",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



