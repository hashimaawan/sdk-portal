# Sticky Sessions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0aWNreVNlc3Npb25z

An object specifying sticky sessions settings for the load balancer.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`StickySessions`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cookieName` | `string \| undefined` | Optional | The name of the cookie sent to the client. This attribute is only returned when using `cookies` for the sticky sessions type. |
| `cookieTtlSeconds` | `number \| undefined` | Optional | The number of seconds until the cookie set by the load balancer expires. This attribute is only returned when using `cookies` for the sticky sessions type. |
| `type` | [`Type16 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-16.md) | Optional | An attribute indicating how and if requests from a client will be persistently served by the same backend Droplet. The possible values are `cookies` or `none`.<br><br>**Default**: `Type16.None` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { StickySessions, Type16 } from 'digitalocean-apilib';

const stickySessions: StickySessions = {
  cookieName: 'DO-LB',
  cookieTtlSeconds: 300,
  type: Type16.Cookies,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



