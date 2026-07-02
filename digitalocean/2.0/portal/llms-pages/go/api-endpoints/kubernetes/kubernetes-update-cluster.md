# Kubernetes Update Cluster

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX3VwZGF0ZV9jbHVzdGVy

To update a Kubernetes cluster, send a PUT request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID` and specify one or more of the
attributes below.

```go
KubernetesUpdateCluster(
    ctx context.Context,
    clusterId uuid.UUID,
    body models.V2KubernetesClustersRequest) (
    models.ApiResponse[models.V2KubernetesClustersResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterId` | `uuid.UUID` | Template, Required | A unique ID that can be used to reference a Kubernetes cluster. |
| `body` | [`models.V2KubernetesClustersRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-kubernetes-clusters-request.md) | Body, Required | - |


# Response Type

**202**: The response will be a JSON object with a key called `kubernetes_cluster`. The
value of this will be an object containing the standard attributes of a
Kubernetes cluster.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2KubernetesClustersResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-kubernetes-clusters-response-1.md).


# Example Usage

```go
ctx := context.Background()

clusterId := uuid.MustParse("bd5f5959-5e1e-4205-a714-a914373942af")

body := models.V2KubernetesClustersRequest{
    AutoUpgrade:           models.ToPointer(true),
    Ha:                    models.ToPointer(true),
    Name:                  "prod-cluster-01",
    SurgeUpgrade:          models.ToPointer(true),
    Tags:                  []string{
        "k8s",
        "k8s:bd5f5959-5e1e-4205-a714-a914373942af",
        "production",
        "web-team",
    },
}

apiResponse, err := kubernetesApi.KubernetesUpdateCluster(ctx, clusterId, body)
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


# Example Response *(as JSON)*

```json
{
  "kubernetes_cluster": {
    "auto_upgrade": true,
    "cluster_subnet": "10.244.0.0/16",
    "created_at": "2018-11-15T16:00:11Z",
    "endpoint": "https://bd5f5959-5e1e-4205-a714-a914373942af.k8s.ondigitalocean.com",
    "ha": false,
    "id": "bd5f5959-5e1e-4205-a714-a914373942af",
    "ipv4": "68.183.121.157",
    "maintenance_policy": {
      "day": "any",
      "duration": "4h0m0s",
      "start_time": "00:00"
    },
    "name": "prod-cluster-01",
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
        ],
        "taints": []
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
        ],
        "taints": []
      }
    ],
    "region": "nyc1",
    "registry_enabled": false,
    "service_subnet": "10.245.0.0/16",
    "status": {
      "state": "running"
    },
    "surge_upgrade": true,
    "tags": [
      "production",
      "web-team",
      "k8s",
      "k8s:bd5f5959-5e1e-4205-a714-a914373942af"
    ],
    "updated_at": "2018-11-15T16:00:11Z",
    "version": "1.18.6-do.0",
    "vpc_uuid": "c33931f2-a26a-4e61-b85c-4e95a2ec431b"
  }
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



