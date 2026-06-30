# Http

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkh0dHA

Additional configuration for protocol http


# Interface Name

`Http`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domain` | `string \| null` | Required | Host header to send in the HTTP request. May not contain spaces, percent or backslash symbols. Can be null, in that case no host header is sent. |
| `path` | `string` | Required | HTTP path to use for health checks. May not contain literal spaces, use percent-encoding instead. |
| `response` | `string \| undefined` | Optional | String that must be contained in HTTP response in order to pass the health check |
| `statusCodes` | `string[] \| undefined` | Optional | List of returned HTTP status codes in order to pass the health check. Supports the wildcards `?` for exactly one character and `*` for multiple ones. The default is to pass the health check for any status code between 2?? and 3??. |
| `tls` | `boolean \| undefined` | Optional | Use HTTPS for health check |


# Example

```ts
import { Http } from 'hetzner-cloud-apilib';

const http: Http = {
  domain: 'example.com',
  path: '/',
  response: '{"status": "ok"}',
  statusCodes: [
    '2??',
    '3??'
  ],
  tls: false,
};
```



