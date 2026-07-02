# Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk9iamVjdA

Metadata about the Kubernetes API object the diagnostic is reported on.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`MObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Kind` | `string` | Optional | The kind of Kubernetes API object |
| `Name` | `string` | Optional | Name of the object |
| `Namespace` | `string` | Optional | The namespace the object resides in the cluster. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Utilities;

MObject mObject = new MObject
{
    Kind = "config map",
    Name = "foo",
    MNamespace = "kube-system",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



