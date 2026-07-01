# O Auth Provider

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/go/x-redirect/JTI0bSUyRk9BdXRoUHJvdmlkZXI

OAuth 2 Authorization endpoint exception.


# Class Name

`OAuthProviderException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`models.OAuthProviderErrorEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/go/models/enumerations/o-auth-provider-error.md) | Required | Gets or sets error code. |
| `ErrorDescription` | `*string` | Optional | Gets or sets human-readable text providing additional information on error.<br>Used to assist the client developer in understanding the error that occurred. |
| `ErrorUri` | `*string` | Optional | Gets or sets a URI identifying a human-readable web page with information about the error, used to provide the client developer with additional information about the error. |


# Example

```go
if err != nil {
    switch typedErr := err.(type) {
    case *errors.OAuthProviderException:
        log.Fatalln(typedErr)
    default:
        log.Fatalln(err)
    }
}
```



