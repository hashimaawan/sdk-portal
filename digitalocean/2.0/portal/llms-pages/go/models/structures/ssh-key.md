# Ssh Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlNzaEtleQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`SshKey`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Fingerprint` | `*string` | Optional, Read-only | A unique identifier that differentiates this key from other keys using  a format that SSH recognizes. The fingerprint is created when the key is added to your account. |
| `Id` | `*int` | Optional, Read-only | A unique identification number for this key. Can be used to embed a  specific SSH key into a Droplet. |
| `Name` | `string` | Required | A human-readable display name for this key, used to easily identify the SSH keys when they are displayed. |
| `PublicKey` | `string` | Required | The entire public key string that was uploaded. Embedded into the root user's `authorized_keys` file if you include this key during Droplet creation. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    sshKey := models.SshKey{
        Fingerprint:           models.ToPointer("3b:16:bf:e4:8b:00:8b:b8:59:8c:a9:d3:f0:19:45:fa"),
        Id:                    models.ToPointer(512189),
        Name:                  "My SSH Public Key",
        PublicKey:             "ssh-rsa AEXAMPLEaC1yc2EAAAADAQABAAAAQQDDHr/jh2Jy4yALcK4JyWbVkPRaWmhck3IgCoeOO3z1e2dBowLh64QAM+Qb72pxekALga2oi4GvT+TlWNhzPH4V example",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



