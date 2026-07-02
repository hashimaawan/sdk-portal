# Single Droplet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlNpbmdsZSUyNTIwRHJvcGxldCUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`SingleDropletRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | The human-readable string you wish to use when displaying the Droplet name. The name, if set to a domain name managed in the DigitalOcean DNS management system, will configure a PTR record for the Droplet. The name set during creation will also determine the hostname for the Droplet in its internal configuration. |
| `Backups` | `*bool` | Optional | A boolean indicating whether automated backups should be enabled for the Droplet.<br><br>**Default**: `false` |
| `Image` | [`models.SingleDropletRequestImage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/oneof-anyof-definitions/single-droplet-request-image.md) | Required | This is a container for one-of cases. |
| `Ipv6` | `*bool` | Optional | A boolean indicating whether to enable IPv6 on the Droplet.<br><br>**Default**: `false` |
| `Monitoring` | `*bool` | Optional | A boolean indicating whether to install the DigitalOcean agent for monitoring.<br><br>**Default**: `false` |
| `PrivateNetworking` | `*bool` | Optional | This parameter has been deprecated. Use `vpc_uuid` instead to specify a VPC network for the Droplet. If no `vpc_uuid` is provided, the Droplet will be placed in your account's default VPC for the region.<br><br>**Default**: `false` |
| `Region` | `*string` | Optional | The slug identifier for the region that you wish to deploy the Droplet in. If the specific datacenter is not not important, a slug prefix (e.g. `nyc`) can be used to deploy the Droplet in any of the that region's locations (`nyc1`, `nyc2`, or `nyc3`). If the region is omitted from the create request completely, the Droplet may deploy in any region. |
| `Size` | `string` | Required | The slug identifier for the size that you wish to select for this Droplet. |
| `SshKeys` | [`[]models.SingleDropletRequestSshKeys`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/oneof-anyof-definitions/single-droplet-request-ssh-keys.md) | Optional | This is Array of a container for any-of cases. |
| `Tags` | `models.Optional[[]string]` | Optional | A flat array of tag names as strings to apply to the Droplet after it is created. Tag names can either be existing or new tags. |
| `UserData` | `*string` | Optional | A string containing 'user data' which may be used to configure the Droplet on first boot, often a 'cloud-config' file or Bash script. It must be plain text and may not exceed 64 KiB in size. |
| `Volumes` | `[]string` | Optional | An array of IDs for block storage volumes that will be attached to the Droplet once created. The volumes must not already be attached to an existing Droplet. |
| `VpcUuid` | `*string` | Optional | A string specifying the UUID of the VPC to which the Droplet will be assigned. If excluded, the Droplet will be assigned to your account's default VPC for the region. |
| `WithDropletAgent` | `*bool` | Optional | A boolean indicating whether to install the DigitalOcean agent used for providing access to the Droplet web console in the control panel. By default, the agent is installed on new Droplets but installation errors (i.e. OS not supported) are ignored. To prevent it from being installed, set to `false`. To make installation errors fatal, explicitly set it to `true`. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    singleDropletRequest := models.SingleDropletRequest{
        Name:                  "example.com",
        Backups:               models.ToPointer(true),
        Image:                 models.SingleDropletRequestImageContainer.FromString("ubuntu-20-04-x64"),
        Ipv6:                  models.ToPointer(true),
        Monitoring:            models.ToPointer(true),
        PrivateNetworking:     models.ToPointer(true),
        Region:                models.ToPointer("nyc3"),
        Size:                  "s-1vcpu-1gb",
        SshKeys:               []models.SingleDropletRequestSshKeys{
            ,
            ,
        },
        Tags:                  models.NewOptional(models.ToPointer([]string{
            "env:prod",
            "web",
        })),
        UserData:              models.ToPointer("#cloud-config\nruncmd:\n  - touch /test.txt\n"),
        Volumes:               []string{
            "12e97116-7280-11ed-b3d0-0a58ac146812",
        },
        VpcUuid:               models.ToPointer("760e09ef-dc84-11e8-981e-3cfdfeaae000"),
        WithDropletAgent:      models.ToPointer(true),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



