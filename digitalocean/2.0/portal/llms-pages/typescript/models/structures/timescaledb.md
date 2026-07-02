# Timescaledb

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlRpbWVzY2FsZWRi

TimescaleDB extension configuration values

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Timescaledb`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `maxBackgroundWorkers` | `number \| undefined` | Optional | The number of background workers for timescaledb operations.  Set to the sum of your number of databases and the total number of concurrent background workers you want running at any given point in time.<br><br>**Constraints**: `>= 1`, `<= 4096` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Timescaledb } from 'digitalocean-apilib';

const timescaledb: Timescaledb = {
  maxBackgroundWorkers: 8,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



