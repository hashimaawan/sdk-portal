# Namespace

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk5hbWVzcGFjZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Namespace`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApiHost` | `string` | Optional | The namespace's API hostname. Each function in a namespace is provided an endpoint at the namespace's hostname. |
| `CreatedAt` | `string` | Optional | UTC time string. |
| `Key` | `string` | Optional | A random alpha numeric string. This key is used in conjunction with the namespace's UUID to authenticate<br>a user to use the namespace via `doctl`, DigitalOcean's official CLI. |
| `Label` | `string` | Optional | The namespace's unique name. |
| `Namespace` | `string` | Optional | A unique string format of UUID with a prefix fn-. |
| `Region` | `string` | Optional | The namespace's datacenter region. |
| `UpdatedAt` | `string` | Optional | UTC time string. |
| `Uuid` | `string` | Optional | The namespace's Universally Unique Identifier. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Namespace mNamespace = new Namespace
{
    ApiHost = "https://api_host.io",
    CreatedAt = "2022-09-14T04:16:45Z",
    Key = "d1zcd455h01mqjfs4s2eaewyejehi5f2uj4etqq3h7cera8iwkub6xg5of1wdde2",
    Label = "my namespace",
    MNamespace = "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
    Region = "nyc1",
    UpdatedAt = "2022-09-14T04:16:45Z",
    Uuid = "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



