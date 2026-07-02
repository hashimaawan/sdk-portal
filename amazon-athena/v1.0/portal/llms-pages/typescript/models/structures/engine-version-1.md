# Engine Version 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24x


# Interface Name

`EngineVersion1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selectedEngineVersion` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `effectiveEngineVersion` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```ts
import { EngineVersion1 } from 'amazon-athenalib';

const engineVersion1: EngineVersion1 = {
  selectedEngineVersion: 'SelectedEngineVersion2',
  effectiveEngineVersion: 'EffectiveEngineVersion8',
};
```



