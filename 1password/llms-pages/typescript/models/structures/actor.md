# Actor

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRkFjdG9y

*This model accepts additional fields of type unknown.*


# Interface Name

`Actor`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account` | `string \| undefined` | Optional | - |
| `id` | `string \| undefined` | Optional | - |
| `jti` | `string \| undefined` | Optional | - |
| `requestIp` | `string \| undefined` | Optional | - |
| `userAgent` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Actor } from 'm-1-password-connectlib';

const actor: Actor = {
  account: 'account0',
  id: '0000193c-0000-0000-0000-000000000000',
  jti: 'jti2',
  requestIp: 'requestIp4',
  userAgent: 'userAgent6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



