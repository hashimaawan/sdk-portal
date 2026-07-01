# Get a List of Symbols for Which We Provide Real-Time Quotes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/net-standard-library/x-redirect/JTI0ZSUyRmZvcmV4JTJGR2V0JTI1MjBhJTI1MjBsaXN0JTI1MjBvZiUyNTIwc3ltYm9scyUyNTIwZm9yJTI1MjB3aGljaCUyNTIwd2UlMjUyMHByb3ZpZGUlMjUyMHJlYWwtdGltZSUyNTIwcXVvdGVz

Symbol List

Find out more: [http://1forge.com/forex-data-api](http://1forge.com/forex-data-api)

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAListOfSymbolsForWhichWeProvideRealTimeQuotesAsync()
```


# Response Type

**200**: A list of symbols

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type List<string>.


# Example Usage

```csharp
try
{
    ApiResponse<List<string>> result = await forexApi.GetAListOfSymbolsForWhichWeProvideRealTimeQuotesAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



