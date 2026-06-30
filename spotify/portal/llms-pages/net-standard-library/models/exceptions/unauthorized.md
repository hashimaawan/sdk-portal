# Unauthorized

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlVuYXV0aG9yaXplZA

*This model accepts additional fields of type object.*


# Class Name

`UnauthorizedException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/error-object.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
try
{
    // make the API call
}
catch (ApiException e)
{
    if (e is UnauthorizedException)
    {
        // TODO: Handle UnauthorizedException
        Console.WriteLine(e.Message);
    }
}
```



