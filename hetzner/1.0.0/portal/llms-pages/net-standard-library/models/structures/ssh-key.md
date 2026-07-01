# Ssh Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNzaEtleQ

*This model accepts additional fields of type object.*


# Class Name

`SshKey`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `Fingerprint` | `string` | Required | Fingerprint of public key |
| `Id` | `int` | Required | ID of the Resource |
| `Labels` | `Dictionary<string, string>` | Required | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `PublicKey` | `string` | Required | Public key |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

SshKey sshKey = new SshKey
{
    Created = "2016-01-30T23:55:00+00:00",
    Fingerprint = "b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f",
    Id = 42,
    Labels = new Dictionary<string, string>
    {
        ["key0"] = "labels4",
        ["key1"] = "labels3",
        ["key2"] = "labels2",
    },
    Name = "my-resource",
    PublicKey = "ssh-rsa AAAjjk76kgf...Xt",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



