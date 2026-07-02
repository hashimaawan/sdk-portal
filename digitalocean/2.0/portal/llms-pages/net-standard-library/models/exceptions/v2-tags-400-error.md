# V2 Tags 400 Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjA0MDAlMjUyMEVycm9y

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2Tags400ErrorException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | `string` | Required | A message providing information about the error. |
| `Messages` | `List<string>` | Optional | A list of error messages. |
| `RootCauses` | `List<string>` | Required | A list of underlying causes for the error, including details to help  resolve it when possible. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
try
{
    // make the API call
}
catch (ApiException e)
{
    if (e is V2Tags400ErrorException)
    {
        // TODO: Handle V2Tags400ErrorException
        Console.WriteLine(e.Message);
    }
}
```



