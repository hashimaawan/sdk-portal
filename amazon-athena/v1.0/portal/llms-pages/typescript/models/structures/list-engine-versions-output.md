# List Engine Versions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc091dHB1dA

*This model accepts additional fields of type unknown.*


# Interface Name

`ListEngineVersionsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `engineVersions` | [`EngineVersion[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/engine-version.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ListEngineVersionsOutput } from 'amazon-athenalib';

const listEngineVersionsOutput: ListEngineVersionsOutput = {
  engineVersions: [
    {
      selectedEngineVersion: 'SelectedEngineVersion2',
      effectiveEngineVersion: 'EffectiveEngineVersion2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  nextToken: 'NextToken0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



