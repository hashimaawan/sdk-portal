# Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkF0dGFjaFRvTmV0d29ya1JlcXVlc3Q


# Class Name

`AttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AliasIps` | `[]string` | Optional | Additional IPs to be assigned to this Server |
| `Ip` | `*string` | Optional | IP to request to be assigned to this Server; if you do not provide this then you will be auto assigned an IP address |
| `Network` | `int` | Required | ID of an existing network to attach the Server to |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    attachToNetworkRequest := models.AttachToNetworkRequest{
        AliasIps:             []string{
            "10.0.1.2",
        },
        Ip:                   models.ToPointer("10.0.1.1"),
        Network:              4711,
    }

}
```



