# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/typescript/x-redirect/JTI0bSUyRk1ldGE

The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances.

*This model accepts additional fields of type unknown.*


# Interface Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `msg` | `string \| undefined` | Optional | HTTP Response Message |
| `responseId` | `string \| undefined` | Optional | A unique ID paired with this response from the API. |
| `status` | `number \| undefined` | Optional | HTTP Response Code |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Meta } from 'giphy-apilib';

const meta: Meta = {
  msg: 'OK',
  responseId: '57eea03c72381f86e05c35d2',
  status: 200,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



