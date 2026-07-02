# V2 Tags 400 Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjA0MDAlMjUyMEVycm9y

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Class Name

`V2Tags400Error`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | `string` | Required | A message providing information about the error. |
| `messages` | `string[] \| null \| undefined` | Optional | A list of error messages. |
| `rootCauses` | `string[]` | Required | A list of underlying causes for the error, including details to help  resolve it when possible. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
try {
  // make the API call
} catch (error) {
  if (error instanceof V2Tags400Error) {
    console.log(error.result);
  }
}
```



