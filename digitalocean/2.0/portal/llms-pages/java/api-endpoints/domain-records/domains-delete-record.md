# Domains Delete Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkRvbWFpbiUyNTIwUmVjb3JkcyUyRmRvbWFpbnNfZGVsZXRlX3JlY29yZA

To delete a record for a domain, send a DELETE request to
`/v2/domains/$DOMAIN_NAME/records/$DOMAIN_RECORD_ID`.

The record will be deleted and the response status will be a 204. This
indicates a successful request with no body returned.

```java
CompletableFuture<ApiResponse<Void>> domainsDeleteRecordAsync(
    final String domainName,
    final int domainRecordId)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domainName` | `String` | Template, Required | The name of the domain itself. |
| `domainRecordId` | `int` | Template, Required | The unique identifier of the domain record. |


# Response Type

**204**: The action was successful and the response body is empty.

`void`


# Example Usage

```java
String domainName = "example.com";
int domainRecordId = 3352896;

domainRecordsApi.domainsDeleteRecordAsync(domainName, domainRecordId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof V21Clicks401ErrorException) {
        V21Clicks401ErrorException v21Clicks401ErrorException = (V21Clicks401ErrorException) cause;
        v21Clicks401ErrorException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



