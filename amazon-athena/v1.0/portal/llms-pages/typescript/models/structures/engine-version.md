# Engine Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24

The Athena engine version for running queries, or the PySpark engine version for running sessions.


# Interface Name

`EngineVersion`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selectedEngineVersion` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `effectiveEngineVersion` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```ts
import { EngineVersion } from 'amazon-athenalib';

const engineVersion: EngineVersion = {
  selectedEngineVersion: 'SelectedEngineVersion0',
  effectiveEngineVersion: 'EffectiveEngineVersion0',
};
```



