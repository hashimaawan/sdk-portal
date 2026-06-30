# Bad Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRkJhZFJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Class Name

`BadRequestError`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/error-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
try {
  // make the API call
} catch (error) {
  if (error instanceof BadRequestError) {
    console.log(error.result);
  }
}
```



