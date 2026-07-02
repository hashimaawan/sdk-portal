# Kubernetes List Node Pools

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX2xpc3Rfbm9kZVBvb2xz

To list all of the node pools in a Kubernetes clusters, send a GET request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools`.

```csharp
KubernetesListNodePoolsAsync(
    Guid clusterId)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `Guid` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |


# Response Type

**200**: The response will be a JSON object with a key called `node_pools`. This will
be set to an array of objects, each of which will contain the standard node
pool attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2KubernetesClustersNodePoolsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-kubernetes-clusters-node-pools-response.md).


# Example Usage

```csharp
Guid clusterId = new Guid("bd5f5959-5e1e-4205-a714-a914373942af");
try
{
    ApiResponse<V2KubernetesClustersNodePoolsResponse> result = await kubernetesApi.KubernetesListNodePoolsAsync(clusterId);
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


# Example Response *(as JSON)*

```json
{
  "node_pools": [
    {
      "auto_scale": false,
      "count": 3,
      "id": "cdda885e-7663-40c8-bc74-3a036c66545d",
      "labels": null,
      "max_nodes": 0,
      "min_nodes": 0,
      "name": "frontend-pool",
      "nodes": [
        {
          "created_at": "2018-11-15T16:00:11Z",
          "droplet_id": "205545370",
          "id": "478247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f",
          "name": "adoring-newton-3niq",
          "status": {
            "state": "running"
          },
          "updated_at": "2018-11-15T16:00:11Z"
        },
        {
          "created_at": "2018-11-15T16:00:11Z",
          "droplet_id": "205545371",
          "id": "ad12e744-c2a9-473d-8aa9-be5680500eb1",
          "name": "adoring-newton-3nim",
          "status": {
            "state": "running"
          },
          "updated_at": "2018-11-15T16:00:11Z"
        },
        {
          "created_at": "2018-11-15T16:00:11Z",
          "droplet_id": "205545372",
          "id": "e46e8d07-f58f-4ff1-9737-97246364400e",
          "name": "adoring-newton-3ni7",
          "status": {
            "state": "running"
          },
          "updated_at": "2018-11-15T16:00:11Z"
        }
      ],
      "size": "s-1vcpu-2gb",
      "tags": [
        "production",
        "web-team",
        "k8s",
        "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
        "k8s:worker"
      ]
    },
    {
      "auto_scale": true,
      "count": 2,
      "id": "f49f4379-7e7f-4af5-aeb6-0354bd840778",
      "labels": {
        "priority": "high",
        "service": "backend"
      },
      "max_nodes": 5,
      "min_nodes": 2,
      "name": "backend-pool",
      "nodes": [
        {
          "created_at": "2018-11-15T16:00:11Z",
          "droplet_id": "205545373",
          "id": "3385619f-8ec3-42ba-bb23-8d21b8ba7518",
          "name": "affectionate-nightingale-3nif",
          "status": {
            "state": "running"
          },
          "updated_at": "2018-11-15T16:00:11Z"
        },
        {
          "created_at": "2018-11-15T16:00:11Z",
          "droplet_id": "205545374",
          "id": "4b8f60ff-ba06-4523-a6a4-b8148244c7e6",
          "name": "affectionate-nightingale-3niy",
          "status": {
            "state": "running"
          },
          "updated_at": "2018-11-15T16:00:11Z"
        }
      ],
      "size": "g-4vcpu-16gb",
      "tags": [
        "production",
        "web-team",
        "k8s",
        "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
        "k8s:worker"
      ]
    }
  ]
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



