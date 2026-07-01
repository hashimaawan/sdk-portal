# Trip GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRiUyRlRyaXBfR0VU

list user's trips

```java
CompletableFuture<ApiResponse<List<Trip>>> tripGetAsync()
```


# Authentication

This endpoint requires [furkot_auth_access_code](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/java/getting-started/quickstart/authorization.md) **OR** [furkot_auth_implicit](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Requires scope

## furkot_auth_access_code

`read:trips`

## furkot_auth_implicit

`read:trips`


# Response Type

**200**: Successful response

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`List<Trip>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/java/models/structures/trip.md).


# Example Usage

```java
api.tripGetAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



