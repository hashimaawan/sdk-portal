# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Registry` | `string` | Optional | The registry name. Must be left empty for the `DOCR` registry type. |
| `RegistryType` | [`RegistryType?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/registry-type.md) | Optional | - DOCKER_HUB: The DockerHub container registry type.<br>- DOCR: The DigitalOcean container registry type. |
| `Repository` | `string` | Optional | The repository name. |
| `Tag` | `string` | Optional | The repository tag. Defaults to `latest` if not provided.<br><br>**Default**: `"latest"` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Image image = new Image
{
    Registry = "registry.hub.docker.com",
    RegistryType = RegistryType.Docr,
    Repository = "origin/master",
    Tag = "latest",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



