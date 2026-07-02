# Load Balancers Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcnNDcmVhdGVCb2R5


# Class Name

`LoadBalancersCreateBody`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`AssignDropletsById`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/assign-droplets-by-id.md) | LoadBalancersCreateBody.fromAssignDropletsById(AssignDropletsById assignDropletsById) |
| [`AssignDropletsByTag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/assign-droplets-by-tag.md) | LoadBalancersCreateBody.fromAssignDropletsByTag(AssignDropletsByTag assignDropletsByTag) |


# AssignDropletsById

## Initialization Code

### Example

```java
LoadBalancersCreateBody.fromAssignDropletsById(
        new AssignDropletsById.Builder(
            Arrays.asList(
                3164444,
                3164445
            ),
            Region2.NYC3,
            Arrays.asList(
                new ForwardingRule.Builder(
                    443,
                    EntryProtocol.HTTPS,
                    80,
                    TargetProtocol.HTTP
                )
                .certificateId("892071a0-bb95-49bc-8021-3afd67a210bf")
                .tlsPassthrough(false)
                .build()
            )
        )
        .algorithm(Algorithm.ROUND_ROBIN)
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2017-02-01T22:22:58Z"))
        .disableLetsEncryptDnsRecords(true)
        .enableBackendKeepalive(true)
        .enableProxyProtocol(true)
        .httpIdleTimeoutSeconds(90)
        .id(UUID.fromString("4de7ac8b-495b-4884-9a69-1050c6793cd6"))
        .ip("104.131.186.241")
        .name("example-lb-01")
        .projectId("4de7ac8b-495b-4884-9a69-1050c6793cd6")
        .redirectHttpToHttps(true)
        .size(Size2.LBSMALL)
        .sizeUnit(3)
        .status(Status12.ENUM_NEW)
        .vpcUuid(UUID.fromString("c33931f2-a26a-4e61-b85c-4e95a2ec431b"))
        .build()
    )
```


# AssignDropletsByTag

## Initialization Code

### Example

```java
LoadBalancersCreateBody.fromAssignDropletsByTag(
        new AssignDropletsByTag.Builder(
            "prod:web",
            Region2.NYC3,
            Arrays.asList(
                new ForwardingRule.Builder(
                    443,
                    EntryProtocol.HTTPS,
                    80,
                    TargetProtocol.HTTP
                )
                .certificateId("892071a0-bb95-49bc-8021-3afd67a210bf")
                .tlsPassthrough(false)
                .build()
            )
        )
        .algorithm(Algorithm.ROUND_ROBIN)
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2017-02-01T22:22:58Z"))
        .disableLetsEncryptDnsRecords(true)
        .enableBackendKeepalive(true)
        .enableProxyProtocol(true)
        .httpIdleTimeoutSeconds(90)
        .id(UUID.fromString("4de7ac8b-495b-4884-9a69-1050c6793cd6"))
        .ip("104.131.186.241")
        .name("example-lb-01")
        .projectId("4de7ac8b-495b-4884-9a69-1050c6793cd6")
        .redirectHttpToHttps(true)
        .size(Size2.LBSMALL)
        .sizeUnit(3)
        .status(Status12.ENUM_NEW)
        .vpcUuid(UUID.fromString("c33931f2-a26a-4e61-b85c-4e95a2ec431b"))
        .build()
    )
```



