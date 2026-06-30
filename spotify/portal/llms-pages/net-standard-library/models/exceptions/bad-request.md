# Bad Request

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkJhZFJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`BadRequestException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`ErrorObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/error-object.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
try
{
    // make the API call
}
catch (ApiException e)
{
    if (e is BadRequestException)
    {
        // TODO: Handle BadRequestException
        Console.WriteLine(e.Message);
    }
}
```



