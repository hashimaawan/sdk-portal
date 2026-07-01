# Create a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkNyZWF0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Creates a new Firewall.

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `server_already_added`        | Server added more than one time to resource                   |
| `incompatible_network_type`   | The Network type is incompatible for the given resource       |
| `firewall_resource_not_found` | The resource the Firewall should be attached to was not found |

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<CreateFirewallResponse>> createAFirewallAsync(
    final CreateFirewallRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateFirewallRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/create-firewall-request.md) | Body, Optional | - |


# Response Type

**201**: The `firewall` key contains the Firewall that was just created

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CreateFirewallResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/create-firewall-response.md).


# Example Usage

```java
CreateFirewallRequest body = new CreateFirewallRequest.Builder(
    "Corporate Intranet Protection"
)
.applyTo(Arrays.asList(
        new ApplyTo.Builder(
            Type7.SERVER
        )
        .server(new Server2.Builder(
                42
            )
            .build())
        .build()
    ))
.labels(ApiHelper.deserialize("{\"env\":\"dev\"}"))
.rules(Arrays.asList(
        new Rule.Builder(
            Direction.IN,
            Protocol.TCP
        )
        .description("Allow port 80")
        .port("80")
        .sourceIps(Arrays.asList(
                "28.239.13.1/32",
                "28.239.14.0/24",
                "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128"
            ))
        .build()
    ))
.build();

firewallsApi.createAFirewallAsync(body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



