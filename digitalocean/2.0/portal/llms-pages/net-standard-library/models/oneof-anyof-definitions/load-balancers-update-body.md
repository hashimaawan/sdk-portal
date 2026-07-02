# Load Balancers Update Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcnNVcGRhdGVCb2R5


# Class Name

`LoadBalancersUpdateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`AssignDropletsById`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/assign-droplets-by-id.md) | LoadBalancersUpdateBody.FromAssignDropletsByID(AssignDropletsById assignDropletsById) |
| [`AssignDropletsByTag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/assign-droplets-by-tag.md) | LoadBalancersUpdateBody.FromAssignDropletsByTag(AssignDropletsByTag assignDropletsByTag) |


# AssignDropletsById

## Initialization Code

### Example

```csharp
LoadBalancersUpdateBody value = LoadBalancersUpdateBody.FromAssignDropletsByID(
    new AssignDropletsById
    {
        DropletIds = new List<int>
        {
            3164444,
            3164445,
        },
        Region = Region2.Nyc3,
        ForwardingRules = new List<ForwardingRule>
        {
            new ForwardingRule
            {
                EntryPort = 443,
                EntryProtocol = EntryProtocol.Https,
                TargetPort = 80,
                TargetProtocol = TargetProtocol.Http,
                CertificateId = "892071a0-bb95-49bc-8021-3afd67a210bf",
                TlsPassthrough = false,
            },
        },
        Algorithm = Algorithm.RoundRobin,
        CreatedAt = DateTime.ParseExact("2017-02-01T22:22:58Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        DisableLetsEncryptDnsRecords = true,
        EnableBackendKeepalive = true,
        EnableProxyProtocol = true,
        HttpIdleTimeoutSeconds = 90,
        Id = new Guid("4de7ac8b-495b-4884-9a69-1050c6793cd6"),
        Ip = "104.131.186.241",
        Name = "example-lb-01",
        ProjectId = "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        RedirectHttpToHttps = true,
        Size = Size2.Lbsmall,
        SizeUnit = 3,
        Status = Status12.New,
        VpcUuid = new Guid("c33931f2-a26a-4e61-b85c-4e95a2ec431b"),
    }
);
```


# AssignDropletsByTag

## Initialization Code

### Example

```csharp
LoadBalancersUpdateBody value = LoadBalancersUpdateBody.FromAssignDropletsByTag(
    new AssignDropletsByTag
    {
        Tag = "prod:web",
        Region = Region2.Nyc3,
        ForwardingRules = new List<ForwardingRule>
        {
            new ForwardingRule
            {
                EntryPort = 443,
                EntryProtocol = EntryProtocol.Https,
                TargetPort = 80,
                TargetProtocol = TargetProtocol.Http,
                CertificateId = "892071a0-bb95-49bc-8021-3afd67a210bf",
                TlsPassthrough = false,
            },
        },
        Algorithm = Algorithm.RoundRobin,
        CreatedAt = DateTime.ParseExact("2017-02-01T22:22:58Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        DisableLetsEncryptDnsRecords = true,
        EnableBackendKeepalive = true,
        EnableProxyProtocol = true,
        HttpIdleTimeoutSeconds = 90,
        Id = new Guid("4de7ac8b-495b-4884-9a69-1050c6793cd6"),
        Ip = "104.131.186.241",
        Name = "example-lb-01",
        ProjectId = "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        RedirectHttpToHttps = true,
        Size = Size2.Lbsmall,
        SizeUnit = 3,
        Status = Status12.New,
        VpcUuid = new Guid("c33931f2-a26a-4e61-b85c-4e95a2ec431b"),
    }
);
```



