# List of TXT Validation Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3QlMjUyMG9mJTI1MjBUWFQlMjUyMHZhbGlkYXRpb24lMjUyMHJlY29yZA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`ListOfTxtValidationRecord`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `txtName` | `string \| undefined` | Optional, Read-only | - |
| `txtValue` | `string \| undefined` | Optional, Read-only | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { ListOfTxtValidationRecord } from 'digitalocean-apilib';

const listOfTxtValidationRecord: ListOfTxtValidationRecord = {
  txtName: '_acme-challenge.app.example.com',
  txtValue: 'lXLOcN6cPv0nproViNcUHcahD9TrIPlNgdwesj0pYpk',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



