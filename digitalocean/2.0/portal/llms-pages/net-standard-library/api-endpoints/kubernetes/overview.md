# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkt1YmVybmV0ZXMlMkZPdmVydmlldw

[DigitalOcean Kubernetes](https://www.digitalocean.com/docs/kubernetes/)
allows you to quickly deploy scalable and secure Kubernetes clusters. By
sending requests to the `/v2/kubernetes/clusters` endpoint, you can list,
create, or delete clusters as well as scale node pools up and down,
recycle individual nodes, and retrieve the kubeconfig file for use with
a cluster.


# Get instance

An instance of the `KubernetesApi` class can be accessed from the API Client.

```
KubernetesApi kubernetesApi = client.KubernetesApi;
```



