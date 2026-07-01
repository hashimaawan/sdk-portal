# O Auth Provider

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRk9BdXRoUHJvdmlkZXI

OAuth 2 Authorization endpoint exception.


# Class Name

`OAuthProviderError`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`OAuthProviderErrorEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/models/enumerations/o-auth-provider-error.md) | Required | Gets or sets error code. |
| `errorDescription` | `string \| undefined` | Optional | Gets or sets human-readable text providing additional information on error.<br>Used to assist the client developer in understanding the error that occurred. |
| `errorUri` | `string \| undefined` | Optional | Gets or sets a URI identifying a human-readable web page with information about the error, used to provide the client developer with additional information about the error. |


# Example

```ts
try {
  // make the API call
} catch (error) {
  if (error instanceof OAuthProviderError) {
    console.log(error.result);
  }
}
```



