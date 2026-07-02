# Load Balancers Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcnNDcmVhdGVCb2R5


# Data Type

`AssignDropletsById | AssignDropletsByTag`


# Cases

| Type |
|  --- |
| [`AssignDropletsById`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/assign-droplets-by-id.md) |
| [`AssignDropletsByTag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/assign-droplets-by-tag.md) |


# AssignDropletsById

## Initialization Code

### Example

```python
value = AssignDropletsById(
    droplet_ids=[
        3164444,
        3164445
    ],
    region=Region2.NYC3,
    forwarding_rules=[
        ForwardingRule(
            entry_port=443,
            entry_protocol=EntryProtocol.HTTPS,
            target_port=80,
            target_protocol=TargetProtocol.HTTP,
            certificate_id='892071a0-bb95-49bc-8021-3afd67a210bf',
            tls_passthrough=False
        )
    ],
    algorithm=Algorithm.ROUND_ROBIN,
    created_at=dateutil.parser.parse('2017-02-01T22:22:58Z'),
    disable_lets_encrypt_dns_records=True,
    enable_backend_keepalive=True,
    enable_proxy_protocol=True,
    http_idle_timeout_seconds=90,
    id='4de7ac8b-495b-4884-9a69-1050c6793cd6',
    ip='104.131.186.241',
    name='example-lb-01',
    project_id='4de7ac8b-495b-4884-9a69-1050c6793cd6',
    redirect_http_to_https=True,
    size=Size2.LBSMALL,
    size_unit=3,
    status=Status12.NEW,
    vpc_uuid='c33931f2-a26a-4e61-b85c-4e95a2ec431b'
)
```


# AssignDropletsByTag

## Initialization Code

### Example

```python
value = AssignDropletsByTag(
    tag='prod:web',
    region=Region2.NYC3,
    forwarding_rules=[
        ForwardingRule(
            entry_port=443,
            entry_protocol=EntryProtocol.HTTPS,
            target_port=80,
            target_protocol=TargetProtocol.HTTP,
            certificate_id='892071a0-bb95-49bc-8021-3afd67a210bf',
            tls_passthrough=False
        )
    ],
    algorithm=Algorithm.ROUND_ROBIN,
    created_at=dateutil.parser.parse('2017-02-01T22:22:58Z'),
    disable_lets_encrypt_dns_records=True,
    enable_backend_keepalive=True,
    enable_proxy_protocol=True,
    http_idle_timeout_seconds=90,
    id='4de7ac8b-495b-4884-9a69-1050c6793cd6',
    ip='104.131.186.241',
    name='example-lb-01',
    project_id='4de7ac8b-495b-4884-9a69-1050c6793cd6',
    redirect_http_to_https=True,
    size=Size2.LBSMALL,
    size_unit=3,
    status=Status12.NEW,
    vpc_uuid='c33931f2-a26a-4e61-b85c-4e95a2ec431b'
)
```



