# Namespace

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk5hbWVzcGFjZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Namespace`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `apiHost` | `string \| undefined` | Optional | The namespace's API hostname. Each function in a namespace is provided an endpoint at the namespace's hostname. |
| `createdAt` | `string \| undefined` | Optional | UTC time string. |
| `key` | `string \| undefined` | Optional | A random alpha numeric string. This key is used in conjunction with the namespace's UUID to authenticate<br>a user to use the namespace via `doctl`, DigitalOcean's official CLI. |
| `label` | `string \| undefined` | Optional | The namespace's unique name. |
| `namespace` | `string \| undefined` | Optional | A unique string format of UUID with a prefix fn-. |
| `region` | `string \| undefined` | Optional | The namespace's datacenter region. |
| `updatedAt` | `string \| undefined` | Optional | UTC time string. |
| `uuid` | `string \| undefined` | Optional | The namespace's Universally Unique Identifier. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Namespace } from 'digitalocean-apilib';

const namespace: Namespace = {
  apiHost: 'https://api_host.io',
  createdAt: '2022-09-14T04:16:45Z',
  key: 'd1zcd455h01mqjfs4s2eaewyejehi5f2uj4etqq3h7cera8iwkub6xg5of1wdde2',
  label: 'my namespace',
  namespace: 'fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx',
  region: 'nyc1',
  updatedAt: '2022-09-14T04:16:45Z',
  uuid: 'xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



