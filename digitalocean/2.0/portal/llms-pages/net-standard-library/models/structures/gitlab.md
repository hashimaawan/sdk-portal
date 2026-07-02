# Gitlab

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdpdGxhYg

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Gitlab`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Branch` | `string` | Optional | The name of the branch to use |
| `DeployOnPush` | `bool?` | Optional | Whether to automatically deploy new commits made to the repo |
| `Repo` | `string` | Optional | The name of the repo in the format owner/repo. Example: `digitalocean/sample-golang` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Gitlab gitlab = new Gitlab
{
    Branch = "main",
    DeployOnPush = true,
    Repo = "digitalocean/sample-golang",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



