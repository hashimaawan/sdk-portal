# Change DNSPTR Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNoYW5nZUROU1BUUlJlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`ChangeDnsptrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `*string` | Required | Hostname to set as a reverse DNS PTR entry, will reset to original default value if `null` |
| `Ip` | `string` | Required | IP address for which to set the reverse DNS entry |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    changeDnsptrRequest := models.ChangeDnsptrRequest{
        DnsPtr:                models.ToPointer("server02.example.com"),
        Ip:                    "1.2.3.4",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



