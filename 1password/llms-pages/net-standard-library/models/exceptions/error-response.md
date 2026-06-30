# Error Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRkVycm9yUmVzcG9uc2U

*This model accepts additional fields of type object.*


# Class Name

`ErrorResponseException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `MessageProperty` | `string` | Optional | A message detailing the error |
| `Status` | `int?` | Optional | HTTP Status Code |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
try
{
    // make the API call
}
catch (ApiException e)
{
    if (e is ErrorResponseException)
    {
        // TODO: Handle ErrorResponseException
        Console.WriteLine(e.Message);
    }
}
```



