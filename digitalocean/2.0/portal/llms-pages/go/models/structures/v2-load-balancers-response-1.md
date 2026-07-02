# V2 Load Balancers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2LoadBalancersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancer` | [`*models.LoadBalancer1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/load-balancer-1.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    v2LoadBalancersResponse1 := models.V2LoadBalancersResponse1{
        LoadBalancer:          models.ToPointer(models.LoadBalancer1{
            Algorithm:                    models.ToPointer(models.Algorithm_RoundRobin),
            CreatedAt:                    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            DisableLetsEncryptDnsRecords: models.ToPointer(false),
            EnableBackendKeepalive:       models.ToPointer(false),
            EnableProxyProtocol:          models.ToPointer(false),
            ForwardingRules:              []models.ForwardingRule{
                models.ForwardingRule{
                    CertificateId:         models.ToPointer("certificate_id4"),
                    EntryPort:             220,
                    EntryProtocol:         models.EntryProtocol_Http2,
                    TargetPort:            104,
                    TargetProtocol:        models.TargetProtocol_Https,
                    TlsPassthrough:        models.ToPointer(false),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.ForwardingRule{
                    CertificateId:         models.ToPointer("certificate_id4"),
                    EntryPort:             220,
                    EntryProtocol:         models.EntryProtocol_Http2,
                    TargetPort:            104,
                    TargetProtocol:        models.TargetProtocol_Https,
                    TlsPassthrough:        models.ToPointer(false),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:         map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



