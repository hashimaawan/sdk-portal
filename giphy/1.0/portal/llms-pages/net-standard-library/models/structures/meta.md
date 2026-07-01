# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk1ldGE

The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances.

*This model accepts additional fields of type object.*


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Msg` | `string` | Optional | HTTP Response Message |
| `ResponseId` | `string` | Optional | A unique ID paired with this response from the API. |
| `Status` | `int?` | Optional | HTTP Response Code |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using GiphyApi.Standard.Models;
using GiphyApi.Standard.Utilities;

Meta meta = new Meta
{
    Msg = "OK",
    ResponseId = "57eea03c72381f86e05c35d2",
    Status = 200,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



