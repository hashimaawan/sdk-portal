# Git

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdpdA

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Git`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Branch` | `string` | Optional | The name of the branch to use |
| `RepoCloneUrl` | `string` | Optional | The clone URL of the repo. Example: `https://github.com/digitalocean/sample-golang.git` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Git git = new Git
{
    Branch = "main",
    RepoCloneUrl = "https://github.com/digitalocean/sample-golang.git",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



