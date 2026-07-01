# Delete a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZEZWxldGUlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Deletes a Floating IP. If it is currently assigned to a Server it will automatically get unassigned.

:information_source: **Note** This endpoint does not require authentication.

```go
DeleteAFloatingIp(
    ctx context.Context,
    id int) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |


# Response Type

**204**: Floating IP deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

id := 112

resp, err := floatingIPsApi.DeleteAFloatingIp(ctx, id)
if err != nil {
    log.Fatalln(err)
} else {
    fmt.Println(resp.StatusCode)
}
```



