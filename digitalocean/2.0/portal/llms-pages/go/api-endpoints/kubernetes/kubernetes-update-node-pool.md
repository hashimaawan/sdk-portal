# Kubernetes Update Node Pool

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX3VwZGF0ZV9ub2RlUG9vbA

To update the name of a node pool, edit the tags applied to it, or adjust its
number of nodes, send a PUT request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools/$NODE_POOL_ID` with the
following attributes.

```go
KubernetesUpdateNodePool(
    ctx context.Context,
    clusterId uuid.UUID,
    nodePoolId uuid.UUID,
    body models.V2KubernetesClustersNodePoolsRequest) (
    models.ApiResponse[models.V2KubernetesClustersNodePoolsResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `uuid.UUID` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `nodePoolId` | `uuid.UUID` | Template, Required | A unique ID that can be used to reference a Kubernetes node pool. |
| `body` | [`models.V2KubernetesClustersNodePoolsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-kubernetes-clusters-node-pools-request.md) | Body, Required | - |


# Response Type

**202**: The response will be a JSON object with a key called `node_pool`. The value of
this will be an object containing the standard attributes of a node pool.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2KubernetesClustersNodePoolsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-kubernetes-clusters-node-pools-response-1.md).


# Example Usage

```go
ctx := context.Background()

clusterId := uuid.MustParse("bd5f5959-5e1e-4205-a714-a914373942af")

nodePoolId := uuid.MustParse("cdda885e-7663-40c8-bc74-3a036c66545d")

body := models.V2KubernetesClustersNodePoolsRequest{
    AutoScale:             models.ToPointer(true),
    Count:                 models.ToPointer(3),
    MaxNodes:              models.ToPointer(6),
    MinNodes:              models.ToPointer(3),
    Name:                  models.ToPointer("frontend-pool"),
    Tags:                  []string{
        "k8s",
        "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
        "k8s-worker",
        "production",
        "web-team",
    },
}

apiResponse, err := kubernetesApi.KubernetesUpdateNodePool(ctx, clusterId, nodePoolId, body)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.V21Clicks401Error:
            log.Fatalln("V21Clicks401ErrorException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
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



