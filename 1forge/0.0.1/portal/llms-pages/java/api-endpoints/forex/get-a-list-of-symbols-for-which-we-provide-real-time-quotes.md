# Get a List of Symbols for Which We Provide Real-Time Quotes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/java/x-redirect/JTI0ZSUyRmZvcmV4JTJGR2V0JTI1MjBhJTI1MjBsaXN0JTI1MjBvZiUyNTIwc3ltYm9scyUyNTIwZm9yJTI1MjB3aGljaCUyNTIwd2UlMjUyMHByb3ZpZGUlMjUyMHJlYWwtdGltZSUyNTIwcXVvdGVz

Symbol List

Find out more: [http://1forge.com/forex-data-api](http://1forge.com/forex-data-api)

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<List<String>>> getAListOfSymbolsForWhichWeProvideRealTimeQuotesAsync()
```


# Response Type

**200**: A list of symbols

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type `List<String>`.


# Example Usage

```java
forexApi.getAListOfSymbolsForWhichWeProvideRealTimeQuotesAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



