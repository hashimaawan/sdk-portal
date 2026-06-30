# OAuth Provider

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRk9BdXRoUHJvdmlkZXI

OAuth 2 Authorization endpoint exception.

*This model accepts additional fields of type unknown.*


# Class Name

`OauthProviderError`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`OauthProviderError`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/enumerations/oauth-provider-error.md) | Required | Gets or sets error code. |
| `errorDescription` | `string \| undefined` | Optional | Gets or sets human-readable text providing additional information on error.<br>Used to assist the client developer in understanding the error that occurred. |
| `errorUri` | `string \| undefined` | Optional | Gets or sets a URI identifying a human-readable web page with information about the error, used to provide the client developer with additional information about the error. |
| `additionalProperties` | `Record<string, unknown \| undefined>` | Optional | - |


# Example

```ts
try {
  // make the API call
} catch (error) {
  if (error instanceof OauthProviderError) {
    console.log(error.result);
  }
}
```



