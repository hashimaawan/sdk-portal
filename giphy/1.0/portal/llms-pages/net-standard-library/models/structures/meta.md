# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk1ldGE

The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances.


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Msg` | `string` | Optional | HTTP Response Message |
| `ResponseId` | `string` | Optional | A unique ID paired with this response from the API. |
| `Status` | `int?` | Optional | HTTP Response Code |


# Example

```csharp
using GiphyAPI.Standard.Models;

Meta meta = new Meta
{
    Msg = "OK",
    ResponseId = "57eea03c72381f86e05c35d2",
    Status = 200,
};
```



