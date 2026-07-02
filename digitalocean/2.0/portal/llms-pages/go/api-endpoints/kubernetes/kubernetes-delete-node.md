# Kubernetes Delete Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX2RlbGV0ZV9ub2Rl

To delete a single node in a pool, send a DELETE request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools/$NODE_POOL_ID/nodes/$NODE_ID`.

Appending the `skip_drain=1` query parameter to the request causes node
draining to be skipped. Omitting the query parameter or setting its value to
`0` carries out draining prior to deletion.

Appending the `replace=1` query parameter to the request causes the node to
be replaced by a new one after deletion. Omitting the query parameter or
setting its value to `0` deletes without replacement.

```go
KubernetesDeleteNode(
    ctx context.Context,
    clusterId uuid.UUID,
    nodePoolId uuid.UUID,
    nodeId uuid.UUID,
    skipDrain *int,
    replace *int) (
    http.Response,
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `uuid.UUID` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `nodePoolId` | `uuid.UUID` | Template, Required | A unique ID that can be used to reference a Kubernetes node pool. |
| `nodeId` | `uuid.UUID` | Template, Required | A unique ID that can be used to reference a node in a Kubernetes node pool. |
| `skipDrain` | `*int` | Query, Optional | Specifies whether or not to drain workloads from a node before it is deleted. Setting it to `1` causes node draining to be skipped. Omitting the query parameter or setting its value to `0` carries out draining prior to deletion.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0`, `<= 1` |
| `replace` | `*int` | Query, Optional | Specifies whether or not to replace a node after it has been deleted. Setting it to `1` causes the node to be replaced by a new one after deletion. Omitting the query parameter or setting its value to `0` deletes without replacement.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0`, `<= 1` |


# Response Type

**202**: The does not indicate the success or failure of any operation, just that the request has been accepted for processing.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

clusterId := uuid.MustParse("bd5f5959-5e1e-4205-a714-a914373942af")

nodePoolId := uuid.MustParse("cdda885e-7663-40c8-bc74-3a036c66545d")

nodeId := uuid.MustParse("478247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f")

skipDrain := 1

replace := 1

resp, err := kubernetesApi.KubernetesDeleteNode(ctx, clusterId, nodePoolId, nodeId, &skipDrain, &replace)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.V21Clicks401Error:
            log.Fatalln("V21Clicks401ErrorException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    fmt.Println(resp.StatusCode)
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



