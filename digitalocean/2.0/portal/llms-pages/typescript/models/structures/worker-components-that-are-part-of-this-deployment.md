# Worker Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRldvcmtlciUyNTIwY29tcG9uZW50cyUyNTIwdGhhdCUyNTIwYXJlJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhpcyUyNTIwZGVwbG95bWVudA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`WorkerComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | - |
| `sourceCommitHash` | `string \| undefined` | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  WorkerComponentsThatArePartOfThisDeployment,
} from 'digitalocean-apilib';

const workerComponentsThatArePartOfThisDeployment: WorkerComponentsThatArePartOfThisDeployment = {
  name: 'queue-runner',
  sourceCommitHash: '54d4a727f457231062439895000d45437c7bb405',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



