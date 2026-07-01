# Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkVycm9y

Error message for the Action if error occurred, otherwise null


# Interface Name

`Error`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | `string` | Required | Fixed machine readable code |
| `message` | `string` | Required | Humanized error message |


# Example

```ts
import { Error } from 'hetzner-cloud-apilib';

const error: Error = {
  code: 'action_failed',
  message: 'Action failed',
};
```



