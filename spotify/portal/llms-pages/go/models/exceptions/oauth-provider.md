# OAuth Provider

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRk9BdXRoUHJvdmlkZXI

OAuth 2 Authorization endpoint exception.

*This model accepts additional fields of type interface{}.*


# Class Name

`OauthProviderException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`models.OauthProviderError`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/enumerations/oauth-provider-error.md) | Required | Gets or sets error code. |
| `ErrorDescription` | `*string` | Optional | Gets or sets human-readable text providing additional information on error.<br>Used to assist the client developer in understanding the error that occurred. |
| `ErrorUri` | `*string` | Optional | Gets or sets a URI identifying a human-readable web page with information about the error, used to provide the client developer with additional information about the error. |
| `AdditionalProperties` | `map[string]*interface{}` | Optional | - |


# Example

```go
if err != nil {
    switch typedErr := err.(type) {
    case *errors.OauthProviderException:
        log.Fatalln(typedErr)
    default:
        log.Fatalln(err)
    }
}
```



