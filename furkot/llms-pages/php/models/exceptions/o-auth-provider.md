# O Auth Provider

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/php/x-redirect/JTI0bSUyRk9BdXRoUHJvdmlkZXI

OAuth 2 Authorization endpoint exception.


# Class Name

`OAuthProviderException`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `error` | [`string(OAuthProviderErrorEnum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/php/models/enumerations/o-auth-provider-error.md) | Required | Gets or sets error code. | getError(): string | setError(string error): void |
| `errorDescription` | `?string` | Optional | Gets or sets human-readable text providing additional information on error.<br>Used to assist the client developer in understanding the error that occurred. | getErrorDescription(): ?string | setErrorDescription(?string errorDescription): void |
| `errorUri` | `?string` | Optional | Gets or sets a URI identifying a human-readable web page with information about the error, used to provide the client developer with additional information about the error. | getErrorUri(): ?string | setErrorUri(?string errorUri): void |


# Example

```php
try {
    // make the API call
} catch (OAuthProviderException $exp) {
    echo 'Caught OAuthProviderException:', $exp;
} catch (ApiException $exp) {
    echo 'Caught ApiException:', $exp;
}
```



