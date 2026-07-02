# Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk9iamVjdA

Metadata about the Kubernetes API object the diagnostic is reported on.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Object`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kind` | `string \| undefined` | Optional | The kind of Kubernetes API object |
| `name` | `string \| undefined` | Optional | Name of the object |
| `namespace` | `string \| undefined` | Optional | The namespace the object resides in the cluster. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Object } from 'digitalocean-apilib';

const object: Object = {
  kind: 'config map',
  name: 'foo',
  namespace: 'kube-system',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



