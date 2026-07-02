# Kubernetes Create Cluster

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX2NyZWF0ZV9jbHVzdGVy

To create a new Kubernetes cluster, send a POST request to
`/v2/kubernetes/clusters`. The request must contain at least one node pool
with at least one worker.

The request may contain a maintenance window policy describing a time period
when disruptive maintenance tasks may be carried out. Omitting the policy
implies that a window will be chosen automatically. See
[here](https://www.digitalocean.com/docs/kubernetes/how-to/upgrade-cluster/)
for details.

```php
function kubernetesCreateCluster(KubernetesCluster $body): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`KubernetesCluster`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/kubernetes-cluster.md) | Body, Required | - |


# Response Type

**201**: The response will be a JSON object with a key called `kubernetes_cluster`. The
value of this will be an object containing the standard attributes of a
Kubernetes cluster.

The IP address and cluster API server endpoint will not be available until the
cluster has finished provisioning. The initial value of the cluster's
`status.state` attribute will be `provisioning`. When the cluster is ready,
this will transition to `running`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2KubernetesClustersResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-kubernetes-clusters-response-1.md).


# Example Usage

```php
$body = KubernetesClusterBuilder::init(
    'prod-cluster-01',
    [
        NodePoolBuilder::init(
            's-1vcpu-2gb',
            3,
            'worker-pool'
        )->build()
    ],
    'nyc1',
    '1.18.6-do.0'
)->build();

$kubernetesApi = $client->getKubernetesApi();
$apiResponse = $kubernetesApi->kubernetesCreateCluster($body);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2KubernetesClustersResponse1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "kubernetes_cluster": {
    "auto_upgrade": false,
    "cluster_subnet": "10.244.0.0/16",
    "created_at": "2018-11-15T16:00:11Z",
    "endpoint": "",
    "ha": false,
    "id": "bd5f5959-5e1e-4205-a714-a914373942af",
    "ipv4": "",
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
        "name": "worker-pool",
        "nodes": [
          {
            "created_at": "2018-11-15T16:00:11Z",
            "droplet_id": "",
            "id": "478247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f",
            "name": "",
            "status": {
              "state": "provisioning"
            },
            "updated_at": "2018-11-15T16:00:11Z"
          },
          {
            "created_at": "2018-11-15T16:00:11Z",
            "droplet_id": "",
            "id": "ad12e744-c2a9-473d-8aa9-be5680500eb1",
            "name": "",
            "status": {
              "state": "provisioning"
            },
            "updated_at": "2018-11-15T16:00:11Z"
          },
          {
            "created_at": "2018-11-15T16:00:11Z",
            "droplet_id": "",
            "id": "e46e8d07-f58f-4ff1-9737-97246364400e",
            "name": "",
            "status": {
              "state": "provisioning"
            },
            "updated_at": "2018-11-15T16:00:11Z"
          }
        ],
        "size": "s-1vcpu-2gb",
        "tags": [
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
      "message": "provisioning",
      "state": "provisioning"
    },
    "surge_upgrade": false,
    "tags": [
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



