# API Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRkFQSVJlcXVlc3Q

Represents a request that was made to the API. Including what Token was used and what resource was accessed.

*This model accepts additional fields of type unknown.*


# Interface Name

`ApiRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/enumerations/action.md) | Optional | - |
| `actor` | [`Actor \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/actor.md) | Optional | - |
| `requestId` | `string \| undefined` | Optional | The unique id used to identify a single request. |
| `resource` | [`Resource \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/resource.md) | Optional | - |
| `result` | [`Result \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/enumerations/result.md) | Optional | - |
| `timestamp` | `string \| undefined` | Optional, Read-only | The time at which the request was processed by the server. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Action, ApiRequest, Result, Type } from 'm-1-password-connectlib';

const apiRequest: ApiRequest = {
  action: Action.Read,
  actor: {
    account: 'account0',
    id: '0000193c-0000-0000-0000-000000000000',
    jti: 'jti2',
    requestIp: 'requestIp4',
    userAgent: 'userAgent6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  requestId: '000002a8-0000-0000-0000-000000000000',
  resource: {
    item: {
      id: 'id2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    itemVersion: 108,
    type: Type.Item,
    vault: {
      id: 'id6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  result: Result.Success,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



