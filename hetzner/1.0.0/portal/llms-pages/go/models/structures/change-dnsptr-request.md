# Change DNSPTR Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNoYW5nZUROU1BUUlJlcXVlc3Q


# Class Name

`ChangeDNSPTRRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `*string` | Required | Hostname to set as a reverse DNS PTR entry, will reset to original default value if `null` |
| `Ip` | `string` | Required | IP address for which to set the reverse DNS entry |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    changeDNSPTRRequest := models.ChangeDNSPTRRequest{
        DnsPtr:               models.ToPointer("server02.example.com"),
        Ip:                   "1.2.3.4",
    }

}
```



