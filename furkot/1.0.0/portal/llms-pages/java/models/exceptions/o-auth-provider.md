# O Auth Provider

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/java/x-redirect/JTI0bSUyRk9BdXRoUHJvdmlkZXI

OAuth 2 Authorization endpoint exception.


# Class Name

`OAuthProviderException`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | [`OAuthProviderErrorEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/java/models/enumerations/o-auth-provider-error.md) | Required | Gets or sets error code. | OAuthProviderErrorEnum getError() | setError(OAuthProviderErrorEnum error) |
| `ErrorDescription` | `String` | Optional | Gets or sets human-readable text providing additional information on error.<br>Used to assist the client developer in understanding the error that occurred. | String getErrorDescription() | setErrorDescription(String errorDescription) |
| `ErrorUri` | `String` | Optional | Gets or sets a URI identifying a human-readable web page with information about the error, used to provide the client developer with additional information about the error. | String getErrorUri() | setErrorUri(String errorUri) |


# Example

```java
try {
    // make the API call
} catch (OAuthProviderException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```



