# Create Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlcXVlc3Q


# Class Name

`CreateServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Automount` | `*bool` | Optional | Auto-mount Volumes after attach |
| `Datacenter` | `*string` | Optional | ID or name of Datacenter to create Server in (must not be used together with location) |
| `Firewalls` | [`[]models.Firewall4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/firewall-4.md) | Optional | Firewalls which should be applied on the Server's public network interface at creation time |
| `Image` | `string` | Required | ID or name of the Image the Server is created from |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Location` | `*string` | Optional | ID or name of Location to create Server in (must not be used together with datacenter) |
| `Name` | `string` | Required | Name of the Server to create (must be unique per Project and a valid hostname as per RFC 1123) |
| `Networks` | `[]int` | Optional | Network IDs which should be attached to the Server private network interface at the creation time |
| `PlacementGroup` | `*int` | Optional | ID of the Placement Group the server should be in |
| `PublicNet` | [`*models.PublicNet5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/public-net-5.md) | Optional | Public Network options |
| `ServerType` | `string` | Required | ID or name of the Server type this Server should be created with |
| `SshKeys` | `[]string` | Optional | SSH key IDs (`integer`) or names (`string`) which should be injected into the Server at creation time |
| `StartAfterCreate` | `*bool` | Optional | Start Server right after creation. Defaults to true. |
| `UserData` | `*string` | Optional | Cloud-Init user data to use during Server creation. This field is limited to 32KiB. |
| `Volumes` | `[]int` | Optional | Volume IDs which should be attached to the Server at the creation time. Volumes must be in the same Location. |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createServerRequest := models.CreateServerRequest{
        Automount:            models.ToPointer(false),
        Datacenter:           models.ToPointer("nbg1-dc3"),
        Firewalls:            []models.Firewall4{
            models.Firewall4{
                Firewall:             models.ToPointer(38),
            },
        },
        Image:                "ubuntu-20.04",
        Labels:               models.ToPointer(interface{}("[key1, val1][key2, val2]")),
        Location:             models.ToPointer("nbg1"),
        Name:                 "my-server",
        Networks:             []int{
            456,
        },
        PlacementGroup:       models.ToPointer(1),
        ServerType:           "cx11",
        SshKeys:              []string{
            "my-ssh-key",
        },
        StartAfterCreate:     models.ToPointer(true),
        UserData:             models.ToPointer("#cloud-config\nruncmd:\n- [touch, /root/cloud-init-worked]\n"),
        Volumes:              []int{
            123,
        },
    }

}
```



