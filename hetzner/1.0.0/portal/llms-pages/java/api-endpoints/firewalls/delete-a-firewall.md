# Delete a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkRlbGV0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Deletes a Firewall.

#### Call specific error codes

| Code                 | Description                               |
|--------------------- |-------------------------------------------|
| `resource_in_use`    | Firewall must not be in use to be deleted |

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<Void> deleteAFirewallAsync(
    final int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**204**: Firewall deleted

`void`


# Example Usage

```java
int id = 112;

firewallsController.deleteAFirewallAsync(id).thenAccept(result -> {
    // TODO success callback handler
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



