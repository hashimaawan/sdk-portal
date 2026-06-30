# Too Many Requests

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRlRvb01hbnlSZXF1ZXN0cw

*This model accepts additional fields of type unknown.*


# Class Name

`TooManyRequestsError`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`ErrorObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/error-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
try {
  // make the API call
} catch (error) {
  if (error instanceof TooManyRequestsError) {
    console.log(error.result);
  }
}
```



