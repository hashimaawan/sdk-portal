# Kubernetes Delete Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX2RlbGV0ZV9ub2Rl

To delete a single node in a pool, send a DELETE request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools/$NODE_POOL_ID/nodes/$NODE_ID`.

Appending the `skip_drain=1` query parameter to the request causes node
draining to be skipped. Omitting the query parameter or setting its value to
`0` carries out draining prior to deletion.

Appending the `replace=1` query parameter to the request causes the node to
be replaced by a new one after deletion. Omitting the query parameter or
setting its value to `0` deletes without replacement.

```csharp
KubernetesDeleteNodeAsync(
    Guid clusterId,
    Guid nodePoolId,
    Guid nodeId,
    int? skipDrain = 0,
    int? replace = 0)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `Guid` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `nodePoolId` | `Guid` | Template, Required | A unique ID that can be used to reference a Kubernetes node pool. |
| `nodeId` | `Guid` | Template, Required | A unique ID that can be used to reference a node in a Kubernetes node pool. |
| `skipDrain` | `int?` | Query, Optional | Specifies whether or not to drain workloads from a node before it is deleted. Setting it to `1` causes node draining to be skipped. Omitting the query parameter or setting its value to `0` carries out draining prior to deletion.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0`, `<= 1` |
| `replace` | `int?` | Query, Optional | Specifies whether or not to replace a node after it has been deleted. Setting it to `1` causes the node to be replaced by a new one after deletion. Omitting the query parameter or setting its value to `0` deletes without replacement.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0`, `<= 1` |


# Response Type

**202**: The does not indicate the success or failure of any operation, just that the request has been accepted for processing.

`Task`


# Example Usage

```csharp
Guid clusterId = new Guid("bd5f5959-5e1e-4205-a714-a914373942af");
Guid nodePoolId = new Guid("cdda885e-7663-40c8-bc74-3a036c66545d");
Guid nodeId = new Guid("478247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f");
int? skipDrain = 1;
int? replace = 1;
try
{
    await kubernetesApi.KubernetesDeleteNodeAsync(
        clusterId,
        nodePoolId,
        nodeId,
        skipDrain,
        replace
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is V21Clicks401ErrorException)
    {
       // TODO: Handle V21Clicks401ErrorException exception here
    }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



