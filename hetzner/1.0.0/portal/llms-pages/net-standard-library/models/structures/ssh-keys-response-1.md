# Ssh Keys Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type object.*


# Class Name

`SshKeysResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SshKey` | [`SshKey`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/ssh-key.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

SshKeysResponse1 sshKeysResponse1 = new SshKeysResponse1
{
    SshKey = new SshKey
    {
        Created = "2016-01-30T23:55:00+00:00",
        Fingerprint = "b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f",
        Id = 42,
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels0",
        },
        Name = "my-resource",
        PublicKey = "ssh-rsa AAAjjk76kgf...Xt",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



