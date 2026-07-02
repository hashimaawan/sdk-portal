# Engine Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkVuZ2luZUNvbmZpZ3VyYXRpb24x

*This model accepts additional fields of type unknown.*


# Interface Name

`EngineConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `coordinatorDpuSize` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `maxConcurrentDpus` | `number` | Required | **Constraints**: `>= 2`, `<= 5000` |
| `defaultExecutorDpuSize` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `additionalConfigs` | [`AdditionalConfigs \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/additional-configs.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { EngineConfiguration1 } from 'amazon-athenalib';

const engineConfiguration1: EngineConfiguration1 = {
  maxConcurrentDpus: 214,
  coordinatorDpuSize: 1,
  defaultExecutorDpuSize: 1,
  additionalConfigs: {
    additionalProperties: {
      'exampleAdditionalProperty': 'AdditionalConfigs_additionalProperties5'
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



