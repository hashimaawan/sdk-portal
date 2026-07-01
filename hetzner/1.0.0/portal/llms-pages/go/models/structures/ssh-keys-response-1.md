# Ssh Keys Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type interface{}.*


# Class Name

`SshKeysResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SshKey` | [`models.SshKey`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/ssh-key.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    sshKeysResponse1 := models.SshKeysResponse1{
        SshKey:                models.SshKey{
            Created:               "2016-01-30T23:55:00+00:00",
            Fingerprint:           "b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f",
            Id:                    42,
            Labels:                map[string]string{
                "key0": "labels0",
            },
            Name:                  "my-resource",
            PublicKey:             "ssh-rsa AAAjjk76kgf...Xt",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



