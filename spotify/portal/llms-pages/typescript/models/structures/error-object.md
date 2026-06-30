# Error Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRkVycm9yT2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`ErrorObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | `number` | Required | The HTTP status code (also returned in the response header; see [Response Status Codes](/documentation/web-api/concepts/api-calls#response-status-codes) for more information).<br><br>**Constraints**: `>= 400`, `<= 599` |
| `message` | `string` | Required | A short description of the cause of the error. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ErrorObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const errorObject: ErrorObject = {
  status: 400,
  message: 'message2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



