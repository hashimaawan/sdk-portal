# Get a List of Symbols for Which We Provide Real-Time Quotes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/#/net-standard-library/x-redirect/JTI0ZSUyRmZvcmV4JTJGR2V0JTI1MjBhJTI1MjBsaXN0JTI1MjBvZiUyNTIwc3ltYm9scyUyNTIwZm9yJTI1MjB3aGljaCUyNTIwd2UlMjUyMHByb3ZpZGUlMjUyMHJlYWwtdGltZSUyNTIwcXVvdGVz

Symbol List

Find out more: [http://1forge.com/forex-data-api](http://1forge.com/forex-data-api)

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAListOfSymbolsForWhichWeProvideRealTimeQuotesAsync()
```


# Response Type

**200**: A list of symbols

`Task<List<string>>`


# Example Usage

```csharp
try
{
    List<string> result = await forexController.GetAListOfSymbolsForWhichWeProvideRealTimeQuotesAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



