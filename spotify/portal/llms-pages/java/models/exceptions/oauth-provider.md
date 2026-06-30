# OAuth Provider

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/java/x-redirect/JTI0bSUyRk9BdXRoUHJvdmlkZXI

OAuth 2 Authorization endpoint exception.

*This model accepts additional fields of type Object.*


# Class Name

`OauthProviderException`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | [`OauthProviderError`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/enumerations/oauth-provider-error.md) | Required | Gets or sets error code. | OauthProviderError getError() | setError(OauthProviderError error) |
| `ErrorDescription` | `String` | Optional | Gets or sets human-readable text providing additional information on error.<br>Used to assist the client developer in understanding the error that occurred. | String getErrorDescription() | setErrorDescription(String errorDescription) |
| `ErrorUri` | `String` | Optional | Gets or sets a URI identifying a human-readable web page with information about the error, used to provide the client developer with additional information about the error. | String getErrorUri() | setErrorUri(String errorUri) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
try {
    // make the API call
} catch (OauthProviderException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```



