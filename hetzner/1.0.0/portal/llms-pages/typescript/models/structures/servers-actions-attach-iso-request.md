# Servers Actions Attach Iso Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEF0dGFjaCUyNTIwSXNvJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`ServersActionsAttachIsoRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `iso` | `string` | Required | ID or name of ISO to attach to the Server as listed in GET `/isos` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ServersActionsAttachIsoRequest } from 'hetzner-cloud-apilib';

const serversActionsAttachIsoRequest: ServersActionsAttachIsoRequest = {
  iso: 'FreeBSD-11.0-RELEASE-amd64-dvd1',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



