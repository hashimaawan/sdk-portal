# Purpose

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRlB1cnBvc2U

Some item types, Login and Password, have fields used for autofill. This property indicates that purpose and is required for some item types.


# Enum Type Name

`Purpose`


# Fields

| Name |
|  --- |
| `Username` |
| `Password` |
| `Notes` |


# Example

```ts
import { Purpose } from 'm-1-password-connectlib';

const purpose = Purpose.Password;
```



