# Assign Droplets by ID

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkFzc2lnbiUyNTIwRHJvcGxldHMlMjUyMGJ5JTI1MjBJRA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`AssignDropletsById`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DropletIds` | `[]int` | Required | An array containing the IDs of the Droplets assigned to the load balancer. |
| `Region` | [`models.Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. |
| `Algorithm` | [`*models.Algorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/algorithm.md) | Optional | This field has been deprecated. You can no longer specify an algorithm for load balancers.<br><br>**Default**: `"round_robin"` |
| `CreatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the load balancer was created. |
| `DisableLetsEncryptDnsRecords` | `*bool` | Optional | A boolean value indicating whether to disable automatic DNS record creation for Let's Encrypt certificates that are added to the load balancer.<br><br>**Default**: `false` |
| `EnableBackendKeepalive` | `*bool` | Optional | A boolean value indicating whether HTTP keepalive connections are maintained to target Droplets.<br><br>**Default**: `false` |
| `EnableProxyProtocol` | `*bool` | Optional | A boolean value indicating whether PROXY Protocol is in use.<br><br>**Default**: `false` |
| `Firewall` | [`*models.Firewall1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/firewall-1.md) | Optional | An object specifying allow and deny rules to control traffic to the load balancer. |
| `ForwardingRules` | [`[]models.ForwardingRule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/forwarding-rule.md) | Required | An array of objects specifying the forwarding rules for a load balancer.<br><br>**Constraints**: *Minimum Items*: `1` |
| `HealthCheck` | [`*models.HealthCheck1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/health-check-1.md) | Optional | An object specifying health check settings for the load balancer. |
| `HttpIdleTimeoutSeconds` | `*int` | Optional | An integer value which configures the idle timeout for HTTP requests to the target droplets.<br><br>**Default**: `60`<br><br>**Constraints**: `>= 30`, `<= 600` |
| `Id` | `*uuid.UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a load balancer. |
| `Ip` | `*string` | Optional, Read-only | An attribute containing the public-facing IP address of the load balancer.<br><br>**Constraints**: *Pattern*: `^$\|^((25[0-5]\|2[0-4][0-9]\|[01]?[0-9][0-9]?)\.){3}(25[0-5]\|2[0-4][0-9]\|[01]?[0-9][0-9]?)$` |
| `Name` | `*string` | Optional | A human-readable name for a load balancer instance. |
| `ProjectId` | `*string` | Optional | The ID of the project that the load balancer is associated with. If no ID is provided at creation, the load balancer associates with the user's default project. If an invalid project ID is provided, the load balancer will not be created. |
| `RedirectHttpToHttps` | `*bool` | Optional | A boolean value indicating whether HTTP requests to the load balancer on port 80 will be redirected to HTTPS on port 443.<br><br>**Default**: `false` |
| `Size` | [`*models.Size2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/size-2.md) | Optional | This field has been replaced by the `size_unit` field for all regions except in AMS2, NYC2, and SFO1. Each available load balancer size now equates to the load balancer having a set number of nodes.<br><br>* `lb-small` = 1 node<br>* `lb-medium` = 3 nodes<br>* `lb-large` = 6 nodes<br><br>You can resize load balancers after creation up to once per hour. You cannot resize a load balancer within the first hour of its creation.<br><br>**Default**: `"lb-small"` |
| `SizeUnit` | `*int` | Optional | How many nodes the load balancer contains. Each additional node increases the load balancer's ability to manage more connections. Load balancers can be scaled up or down, and you can change the number of nodes after creation up to once per hour. This field is currently not available in the AMS2, NYC2, or SFO1 regions. Use the `size` field to scale load balancers that reside in these regions.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `Status` | [`*models.Status12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-12.md) | Optional, Read-only | A status string indicating the current state of the load balancer. This can be `new`, `active`, or `errored`. |
| `StickySessions` | [`*models.StickySessions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/sticky-sessions.md) | Optional | An object specifying sticky sessions settings for the load balancer. |
| `VpcUuid` | `*uuid.UUID` | Optional | A string specifying the UUID of the VPC to which the load balancer is assigned. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
    "github.com/google/uuid"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    assignDropletsById := models.AssignDropletsById{
        DropletIds:                   []int{
            3164444,
            3164445,
        },
        Region:                       models.Region2_Nyc3,
        Algorithm:                    models.ToPointer(models.Algorithm_RoundRobin),
        CreatedAt:                    models.ToPointer(parseTime(time.RFC3339, "2017-02-01T22:22:58Z", func(err error) { log.Fatalln(err) })),
        DisableLetsEncryptDnsRecords: models.ToPointer(true),
        EnableBackendKeepalive:       models.ToPointer(true),
        EnableProxyProtocol:          models.ToPointer(true),
        ForwardingRules:              []models.ForwardingRule{
            models.ForwardingRule{
                CertificateId:         models.ToPointer("892071a0-bb95-49bc-8021-3afd67a210bf"),
                EntryPort:             443,
                EntryProtocol:         models.EntryProtocol_Https,
                TargetPort:            80,
                TargetProtocol:        models.TargetProtocol_Http,
                TlsPassthrough:        models.ToPointer(false),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        HttpIdleTimeoutSeconds:       models.ToPointer(90),
        Id:                           models.ToPointer(uuid.MustParse("4de7ac8b-495b-4884-9a69-1050c6793cd6")),
        Ip:                           models.ToPointer("104.131.186.241"),
        Name:                         models.ToPointer("example-lb-01"),
        ProjectId:                    models.ToPointer("4de7ac8b-495b-4884-9a69-1050c6793cd6"),
        RedirectHttpToHttps:          models.ToPointer(true),
        Size:                         models.ToPointer(models.Size2_Lbsmall),
        SizeUnit:                     models.ToPointer(3),
        Status:                       models.ToPointer(models.Status12_New),
        VpcUuid:                      models.ToPointer(uuid.MustParse("c33931f2-a26a-4e61-b85c-4e95a2ec431b")),
        AdditionalProperties:         map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



