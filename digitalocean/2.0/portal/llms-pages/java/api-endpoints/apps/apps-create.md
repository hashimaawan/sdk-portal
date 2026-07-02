# Apps Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2NyZWF0ZQ

Create a new app by submitting an app specification. For documentation on app specifications (`AppSpec` objects), please refer to [the product documentation](https://docs.digitalocean.com/products/app-platform/reference/app-spec/).

```java
CompletableFuture<ApiResponse<V2AppsResponse1>> appsCreateAsync(
    final V2AppsRequest body,
    final Accept accept,
    final ContentType contentType)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V2AppsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-apps-request.md) | Body, Required | - |
| `accept` | [`Accept`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/accept.md) | Header, Optional | The content-type that should be used by the response. By default, the response will be `application/json`. `application/yaml` is also supported. |
| `contentType` | [`ContentType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/content-type.md) | Header, Optional | The content-type used for the request. By default, the requests are assumed to use `application/json`. `application/yaml` is also supported. |


# Response Type

**200**: A JSON or YAML of a `spec` object.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2AppsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-apps-response-1.md).


# Example Usage

```java
V2AppsRequest body = new V2AppsRequest.Builder(
    new AppSpec.Builder(
        "web-app"
    )
    .region(Region1.NYC)
    .services(Arrays.asList(
            new Service.Builder(
                "api"
            )
            .environmentSlug("node-js")
            .github(new Github.Builder()
                    .branch("main")
                    .deployOnPush(true)
                    .repo("digitalocean/sample-golang")
                    .build())
            .runCommand("bin/api")
            .instanceCount(2L)
            .instanceSizeSlug(InstanceSizeSlug.BASICXXS)
            .routes(Arrays.asList(
                    new ACriterionForRoutingHttpTrafficToAComponent.Builder()
                        .path("/api")
                        .build()
                ))
            .build()
        ))
    .build()
)
.build();

Accept accept = Accept.ENUM_APPLICATIONJSON;
ContentType contentType = ContentType.ENUM_APPLICATIONJSON;

appsApi.appsCreateAsync(body, accept, contentType).thenAccept(result -> {
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
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



