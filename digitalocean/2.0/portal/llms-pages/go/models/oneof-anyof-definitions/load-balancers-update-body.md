# Load Balancers Update Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcnNVcGRhdGVCb2R5


# Class Name

`LoadBalancersUpdateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.AssignDropletsById`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/assign-droplets-by-id.md) | models.LoadBalancersUpdateBodyContainer.FromAssignDropletsById(models.AssignDropletsById assignDropletsById) |
| [`models.AssignDropletsByTag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/assign-droplets-by-tag.md) | models.LoadBalancersUpdateBodyContainer.FromAssignDropletsByTag(models.AssignDropletsByTag assignDropletsByTag) |


# models.AssignDropletsById

## Initialization Code

### Example

```go
value := models.LoadBalancersUpdateBodyContainer.FromAssignDropletsById(models.AssignDropletsById{
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
})
```


# models.AssignDropletsByTag

## Initialization Code

### Example

```go
value := models.LoadBalancersUpdateBodyContainer.FromAssignDropletsByTag(models.AssignDropletsByTag{
    Tag:                          "prod:web",
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
})
```



