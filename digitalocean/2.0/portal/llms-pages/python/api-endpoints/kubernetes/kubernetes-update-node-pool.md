# Kubernetes Update Node Pool

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX3VwZGF0ZV9ub2RlUG9vbA

To update the name of a node pool, edit the tags applied to it, or adjust its
number of nodes, send a PUT request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools/$NODE_POOL_ID` with the
following attributes.

```python
def kubernetes_update_node_pool(self,
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
| `body` | [`V2KubernetesClustersNodePoolsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-kubernetes-clusters-node-pools-request.md) | Body, Required | - |


# Response Type

**202**: The response will be a JSON object with a key called `node_pool`. The value of
this will be an object containing the standard attributes of a node pool.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2KubernetesClustersNodePoolsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-kubernetes-clusters-node-pools-response-1.md).


# Example Usage

```python
cluster_id = 'bd5f5959-5e1e-4205-a714-a914373942af'

node_pool_id = 'cdda885e-7663-40c8-bc74-3a036c66545d'

body = V2KubernetesClustersNodePoolsRequest(
    auto_scale=True,
    count=3,
    max_nodes=6,
    min_nodes=3,
    name='frontend-pool',
    tags=[
        'k8s',
        'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
        'k8s-worker',
        'production',
        'web-team'
    ]
)

result = kubernetes_api.kubernetes_update_node_pool(
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



