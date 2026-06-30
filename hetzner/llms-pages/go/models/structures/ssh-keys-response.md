# Ssh Keys Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2U


# Class Name

`SshKeysResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/meta.md) | Optional | - |
| `SshKeys` | [`[]models.SshKey`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/ssh-key.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    sshKeysResponse := models.SshKeysResponse{
        Meta:                 models.ToPointer(models.Meta{
            Pagination:           models.Pagination{
                LastPage:             models.ToPointer(float64(77.7)),
                NextPage:             models.ToPointer(float64(209.18)),
                Page:                 float64(17.58),
                PerPage:              float64(13.34),
                PreviousPage:         models.ToPointer(float64(50.02)),
                TotalEntries:         models.ToPointer(float64(206.64)),
            },
        }),
        SshKeys:              []models.SshKey{
            models.SshKey{
                Created:              "2016-01-30T23:55:00+00:00",
                Fingerprint:          "b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f",
                Id:                   42,
                Labels:               map[string]string{
                    "key0": "labels4",
                    "key1": "labels5",
                    "key2": "labels6",
                },
                Name:                 "my-resource",
                PublicKey:            "ssh-rsa AAAjjk76kgf...Xt",
            },
        },
    }

}
```



