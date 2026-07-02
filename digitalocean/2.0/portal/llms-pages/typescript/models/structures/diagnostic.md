# Diagnostic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkRpYWdub3N0aWM

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Diagnostic`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkName` | `string \| undefined` | Optional | The clusterlint check that resulted in the diagnostic. |
| `message` | `string \| undefined` | Optional | Feedback about the object for users to fix. |
| `object` | [`Object \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | Metadata about the Kubernetes API object the diagnostic is reported on. |
| `severity` | `string \| undefined` | Optional | Can be one of error, warning or suggestion. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Diagnostic } from 'digitalocean-apilib';

const diagnostic: Diagnostic = {
  checkName: 'unused-config-map',
  message: 'Unused config map',
  object: {
    kind: 'kind0',
    name: 'name2',
    namespace: 'namespace0',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  severity: 'warning',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



