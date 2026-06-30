# Health Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRkhlYWx0aCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type unknown.*


# Interface Name

`HealthResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dependencies` | [`ServiceDependency[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/service-dependency.md) | Optional | - |
| `name` | `string` | Required | - |
| `version` | `string` | Required | The Connect server's version |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { HealthResponse } from 'm-1-password-connectlib';

const healthResponse: HealthResponse = {
  name: 'name4',
  version: 'version0',
  dependencies: [
    {
      message: 'message6',
      service: 'service6',
      status: 'status8',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



