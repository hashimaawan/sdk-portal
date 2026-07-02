# A Criterion for Routing HTTP Traffic to a Component

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkElMjUyMGNyaXRlcmlvbiUyNTIwZm9yJTI1MjByb3V0aW5nJTI1MjBIVFRQJTI1MjB0cmFmZmljJTI1MjB0byUyNTIwYSUyNTIwY29tcG9uZW50Lg

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`ACriterionForRoutingHttpTrafficToAComponent`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `path` | `string \| undefined` | Optional | An HTTP path prefix. Paths must start with / and must be unique across all components within an app. |
| `preservePathPrefix` | `boolean \| undefined` | Optional | An optional flag to preserve the path that is forwarded to the backend service. By default, the HTTP request path will be trimmed from the left when forwarded to the component. For example, a component with `path=/api` will have requests to `/api/list` trimmed to `/list`. If this value is `true`, the path will remain `/api/list`. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  ACriterionForRoutingHttpTrafficToAComponent,
} from 'digitalocean-apilib';

const aCriterionForRoutingHttpTrafficToAComponent: ACriterionForRoutingHttpTrafficToAComponent = {
  path: '/api',
  preservePathPrefix: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



