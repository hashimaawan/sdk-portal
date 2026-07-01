# Ssh Keys Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type object.*


# Class Name

`SshKeysRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `object` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the SSH key |
| `PublicKey` | `string` | Required | Public key |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

SshKeysRequest sshKeysRequest = new SshKeysRequest
{
    Name = "My ssh key",
    PublicKey = "ssh-rsa AAAjjk76kgf...Xt",
    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



