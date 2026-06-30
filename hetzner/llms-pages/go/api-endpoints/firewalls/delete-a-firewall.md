# Delete a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkRlbGV0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Deletes a Firewall.

#### Call specific error codes

| Code                 | Description                               |
|--------------------- |-------------------------------------------|
| `resource_in_use`    | Firewall must not be in use to be deleted |

:information_source: **Note** This endpoint does not require authentication.

```go
DeleteAFirewall(
    ctx context.Context,
    id int) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**204**: Firewall deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

id := 112

resp, err := firewallsController.DeleteAFirewall(ctx, id)
if err != nil {
    log.Fatalln(err)
} else {
    fmt.Println(resp.StatusCode)
}
```



