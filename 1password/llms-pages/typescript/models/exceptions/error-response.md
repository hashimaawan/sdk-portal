# Error Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRkVycm9yUmVzcG9uc2U

*This model accepts additional fields of type unknown.*


# Class Name

`ErrorResponseError`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `string \| undefined` | Optional | A message detailing the error |
| `status` | `number \| undefined` | Optional | HTTP Status Code |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
try {
  // make the API call
} catch (error) {
  if (error instanceof ErrorResponseError) {
    console.log(error.result);
  }
}
```



