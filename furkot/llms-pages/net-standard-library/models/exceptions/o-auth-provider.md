# O Auth Provider

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/net-standard-library/x-redirect/JTI0bSUyRk9BdXRoUHJvdmlkZXI

OAuth 2 Authorization endpoint exception.


# Class Name

`OAuthProviderException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`OAuthProviderErrorEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/net-standard-library/models/enumerations/o-auth-provider-error.md) | Required | Gets or sets error code. |
| `ErrorDescription` | `string` | Optional | Gets or sets human-readable text providing additional information on error.<br>Used to assist the client developer in understanding the error that occurred. |
| `ErrorUri` | `string` | Optional | Gets or sets a URI identifying a human-readable web page with information about the error, used to provide the client developer with additional information about the error. |


# Example

```csharp
try
{
    // make the API call
}
catch (ApiException e)
{
    if (e is OAuthProviderException)
    {
        // TODO: Handle OAuthProviderException
        Console.WriteLine(e.Message);
    }
}
```



