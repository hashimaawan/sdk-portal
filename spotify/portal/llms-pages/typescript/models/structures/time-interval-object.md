# Time Interval Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlRpbWVJbnRlcnZhbE9iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`TimeIntervalObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `start` | `number \| undefined` | Optional | The starting point (in seconds) of the time interval. |
| `duration` | `number \| undefined` | Optional | The duration (in seconds) of the time interval. |
| `confidence` | `number \| undefined` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the interval.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  TimeIntervalObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const timeIntervalObject: TimeIntervalObject = {
  start: 0.49567,
  duration: 2.18749,
  confidence: 0.925,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



