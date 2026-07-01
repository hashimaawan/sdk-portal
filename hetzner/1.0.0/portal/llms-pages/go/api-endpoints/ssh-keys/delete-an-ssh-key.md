# Delete an SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkRlbGV0ZSUyNTIwYW4lMjUyMFNTSCUyNTIwa2V5

Deletes an SSH key. It cannot be used anymore.

:information_source: **Note** This endpoint does not require authentication.

```go
DeleteAnSshKey(
    ctx context.Context,
    id string) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | ID of the SSH key |


# Response Type

**204**: SSH key deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

id := "id0"

resp, err := sshKeysApi.DeleteAnSshKey(ctx, id)
if err != nil {
    log.Fatalln(err)
} else {
    fmt.Println(resp.StatusCode)
}
```



