# Update a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRlVwZGF0ZSUyNTIwYSUyNTIwUHJpbWFyeSUyNTIwSVA

Updates the Primary IP.

Note that when updating labels, the Primary IP's current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

If the Primary IP object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<PrimaryIpResponse>> updateAPrimaryIpAsync(
    final int id,
    final UpdatePrimaryIpRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |
| `body` | [`UpdatePrimaryIpRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/update-primary-ip-request.md) | Body, Optional | - |


# Response Type

**200**: The `primary_ip` key contains the Primary IP that was just updated

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PrimaryIpResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/primary-ip-response.md).


# Example Usage

```java
int id = 112;
UpdatePrimaryIpRequest body = new UpdatePrimaryIpRequest.Builder()
    .autoDelete(true)
    .labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
    .name("my-ip")
    .build();

primaryIPsApi.updateAPrimaryIpAsync(id, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



