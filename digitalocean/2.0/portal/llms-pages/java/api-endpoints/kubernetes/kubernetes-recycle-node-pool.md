# Kubernetes Recycle Node Pool

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX3JlY3ljbGVfbm9kZV9wb29s

**This endpoint is deprecated.**

The endpoint has been deprecated. Please use the DELETE
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools/$NODE_POOL_ID/nodes/$NODE_ID`
method instead.

```java
CompletableFuture<ApiResponse<Void>> kubernetesRecycleNodePoolAsync(
    final UUID clusterId,
    final UUID nodePoolId,
    final V2KubernetesClustersNodePoolsRecycleRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `UUID` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `nodePoolId` | `UUID` | Template, Required | A unique ID that can be used to reference a Kubernetes node pool. |
| `body` | [`V2KubernetesClustersNodePoolsRecycleRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-kubernetes-clusters-node-pools-recycle-request.md) | Body, Required | - |


# Response Type

**202**: The does not indicate the success or failure of any operation, just that the request has been accepted for processing.

`void`


# Example Usage

```java
UUID clusterId = UUID.fromString("bd5f5959-5e1e-4205-a714-a914373942af");
UUID nodePoolId = UUID.fromString("cdda885e-7663-40c8-bc74-3a036c66545d");
V2KubernetesClustersNodePoolsRecycleRequest body = new V2KubernetesClustersNodePoolsRecycleRequest.Builder()
    .nodes(Arrays.asList(
        "d8db5e1a-6103-43b5-a7b3-8a948210a9fc"
    ))
    .build();

kubernetesApi.kubernetesRecycleNodePoolAsync(clusterId, nodePoolId, body).thenAccept(result -> {
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
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



