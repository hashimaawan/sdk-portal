# Kubernetes Cluster User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkt1YmVybmV0ZXNDbHVzdGVyVXNlcg

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`KubernetesClusterUser`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `groups` | `string[] \| undefined` | Optional | A list of in-cluster groups that the user belongs to. |
| `username` | `string \| undefined` | Optional | The username for the cluster admin user. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { KubernetesClusterUser } from 'digitalocean-apilib';

const kubernetesClusterUser: KubernetesClusterUser = {
  groups: [
    'k8saas:authenticated'
  ],
  username: 'sammy@digitalocean.com',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



