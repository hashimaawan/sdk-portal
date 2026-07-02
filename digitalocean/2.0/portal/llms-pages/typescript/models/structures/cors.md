# Cors

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkNvcnM

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Cors`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allowCredentials` | `boolean \| undefined` | Optional | Whether browsers should expose the response to the client-side JavaScript code when the request’s credentials mode is include. This configures the `Access-Control-Allow-Credentials` header. |
| `allowHeaders` | `string[] \| undefined` | Optional | The set of allowed HTTP request headers. This configures the `Access-Control-Allow-Headers` header. |
| `allowMethods` | `string[] \| undefined` | Optional | The set of allowed HTTP methods. This configures the `Access-Control-Allow-Methods` header. |
| `allowOrigins` | [`AllowOrigin[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/allow-origin.md) | Optional | The set of allowed CORS origins. |
| `exposeHeaders` | `string[] \| undefined` | Optional | The set of HTTP response headers that browsers are allowed to access. This configures the `Access-Control-Expose-Headers` header. |
| `maxAge` | `string \| undefined` | Optional | An optional duration specifying how long browsers can cache the results of a preflight request. This configures the `Access-Control-Max-Age` header. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Cors } from 'digitalocean-apilib';

const cors: Cors = {
  allowCredentials: false,
  allowHeaders: [
    'Content-Type',
    'X-Custom-Header'
  ],
  allowMethods: [
    'GET',
    'OPTIONS',
    'POST',
    'PUT',
    'PATCH',
    'DELETE'
  ],
  allowOrigins: [
    {
      exact: 'https://www.example.com',
      prefix: 'prefix6',
      regex: 'regex4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      exact: 'exact8',
      prefix: 'prefix6',
      regex: '^.*example.com',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  exposeHeaders: [
    'Content-Encoding',
    'X-Custom-Header'
  ],
  maxAge: '5h30m',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



