# Load Balancers Update Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcnNVcGRhdGVCb2R5


# Class Name

`LoadBalancersUpdateBody`


# Cases

| Type |
|  --- |
| [`AssignDropletsById`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/assign-droplets-by-id.md) |
| [`AssignDropletsByTag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/assign-droplets-by-tag.md) |


# AssignDropletsById

## Initialization Code

### Example

```ts
const value: LoadBalancersUpdateBody = {
  dropletIds: [
    3164444,
    3164445
  ],
  region: Region2.Nyc3,
  forwardingRules: [
    {
      entryPort: 443,
      entryProtocol: EntryProtocol.Https,
      targetPort: 80,
      targetProtocol: TargetProtocol.Http,
      certificateId: '892071a0-bb95-49bc-8021-3afd67a210bf',
      tlsPassthrough: false,
    }
  ],
  algorithm: Algorithm.RoundRobin,
  createdAt: '2017-02-01T22:22:58Z',
  disableLetsEncryptDnsRecords: true,
  enableBackendKeepalive: true,
  enableProxyProtocol: true,
  httpIdleTimeoutSeconds: 90,
  id: '4de7ac8b-495b-4884-9a69-1050c6793cd6',
  ip: '104.131.186.241',
  name: 'example-lb-01',
  projectId: '4de7ac8b-495b-4884-9a69-1050c6793cd6',
  redirectHttpToHttps: true,
  size: Size2.Lbsmall,
  sizeUnit: 3,
  status: Status12.New,
  vpcUuid: 'c33931f2-a26a-4e61-b85c-4e95a2ec431b',
};
```


# AssignDropletsByTag

## Initialization Code

### Example

```ts
const value: LoadBalancersUpdateBody = {
  tag: 'prod:web',
  region: Region2.Nyc3,
  forwardingRules: [
    {
      entryPort: 443,
      entryProtocol: EntryProtocol.Https,
      targetPort: 80,
      targetProtocol: TargetProtocol.Http,
      certificateId: '892071a0-bb95-49bc-8021-3afd67a210bf',
      tlsPassthrough: false,
    }
  ],
  algorithm: Algorithm.RoundRobin,
  createdAt: '2017-02-01T22:22:58Z',
  disableLetsEncryptDnsRecords: true,
  enableBackendKeepalive: true,
  enableProxyProtocol: true,
  httpIdleTimeoutSeconds: 90,
  id: '4de7ac8b-495b-4884-9a69-1050c6793cd6',
  ip: '104.131.186.241',
  name: 'example-lb-01',
  projectId: '4de7ac8b-495b-4884-9a69-1050c6793cd6',
  redirectHttpToHttps: true,
  size: Size2.Lbsmall,
  sizeUnit: 3,
  status: Status12.New,
  vpcUuid: 'c33931f2-a26a-4e61-b85c-4e95a2ec431b',
};
```



