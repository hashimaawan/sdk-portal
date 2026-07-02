# Kubernetes Recycle Node Pool

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX3JlY3ljbGVfbm9kZV9wb29s

**This endpoint is deprecated.**

The endpoint has been deprecated. Please use the DELETE
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools/$NODE_POOL_ID/nodes/$NODE_ID`
method instead.

```python
def kubernetes_recycle_node_pool(self,
                                cluster_id,
                                node_pool_id,
                                body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cluster_id` | `uuid\|str` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `node_pool_id` | `uuid\|str` | Template, Required | A unique ID that can be used to reference a Kubernetes node pool. |
| `body` | [`V2KubernetesClustersNodePoolsRecycleRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-kubernetes-clusters-node-pools-recycle-request.md) | Body, Required | - |


# Response Type

**202**: The does not indicate the success or failure of any operation, just that the request has been accepted for processing.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
cluster_id = 'bd5f5959-5e1e-4205-a714-a914373942af'

node_pool_id = 'cdda885e-7663-40c8-bc74-3a036c66545d'

body = V2KubernetesClustersNodePoolsRecycleRequest(
    nodes=[
        'd8db5e1a-6103-43b5-a7b3-8a948210a9fc'
    ]
)

result = kubernetes_api.kubernetes_recycle_node_pool(
    cluster_id,
    node_pool_id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |



