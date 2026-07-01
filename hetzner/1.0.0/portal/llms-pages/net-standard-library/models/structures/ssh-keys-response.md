# Ssh Keys Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2U


# Class Name

`SshKeysResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |
| `SshKeys` | [`List<SshKey>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/ssh-key.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

SshKeysResponse sshKeysResponse = new SshKeysResponse
{
    SshKeys = new List<SshKey>
    {
        new SshKey
        {
            Created = "2016-01-30T23:55:00+00:00",
            Fingerprint = "b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f",
            Id = 42,
            Labels = new Dictionary<string, string>
            {
                ["key0"] = "labels4",
                ["key1"] = "labels5",
                ["key2"] = "labels6",
            },
            Name = "my-resource",
            PublicKey = "ssh-rsa AAAjjk76kgf...Xt",
        },
    },
    Meta = new Meta
    {
        Pagination = new Pagination
        {
            LastPage = 77.7,
            NextPage = 209.18,
            Page = 17.58,
            PerPage = 13.34,
            PreviousPage = 50.02,
            TotalEntries = 206.64,
        },
    },
};
```



