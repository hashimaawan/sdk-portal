# V2 1 Clicks Kubernetes Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjAxJTI1MjBDbGlja3MlMjUyMEt1YmVybmV0ZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V21ClicksKubernetesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `addonSlugs` | `string[]` | Required | An array of 1-Click Application slugs to be installed to the Kubernetes cluster. |
| `clusterUuid` | `string` | Required | A unique ID for the Kubernetes cluster to which the 1-Click Applications will be installed. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V21ClicksKubernetesRequest } from 'digitalocean-apilib';

const v21ClicksKubernetesRequest: V21ClicksKubernetesRequest = {
  addonSlugs: [
    'kube-state-metrics',
    'loki'
  ],
  clusterUuid: '50a994b6-c303-438f-9495-7e896cfe6b08',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



