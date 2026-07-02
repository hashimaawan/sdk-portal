# Available Upgrade Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkF2YWlsYWJsZVVwZ3JhZGVWZXJzaW9u

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`AvailableUpgradeVersion`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kubernetesVersion` | `string \| undefined` | Optional | The upstream version string for the version of Kubernetes provided by a given slug. |
| `slug` | `string \| undefined` | Optional | The slug identifier for an available version of Kubernetes for use when creating or updating a cluster. The string contains both the upstream version of Kubernetes as well as the DigitalOcean revision. |
| `supportedFeatures` | `string[] \| undefined` | Optional | The features available with the version of Kubernetes provided by a given slug. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { AvailableUpgradeVersion } from 'digitalocean-apilib';

const availableUpgradeVersion: AvailableUpgradeVersion = {
  kubernetesVersion: '1.16.13',
  slug: '1.16.13-do.0',
  supportedFeatures: [
    'cluster-autoscaler',
    'docr-integration',
    'token-authentication'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



