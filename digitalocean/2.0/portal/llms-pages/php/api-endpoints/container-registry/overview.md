# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkNvbnRhaW5lciUyNTIwUmVnaXN0cnklMkZPdmVydmlldw

DigitalOcean offers the ability for you to create a
[private container registry](https://www.digitalocean.com/docs/images/container-registry/quickstart/)
to store your Docker images for use with your Kubernetes clusters. This
container registry runs inside the same datacenters as your cluster,
ensuring reliable and performant rollout of image deployments.

You can only create one registry per DigitalOcean account, but you can use
that registry to create as many repositories as you wish.


# Get singleton instance

The singleton instance of the `ContainerRegistryApi` class can be accessed from the API Client.

```
$containerRegistryApi = $client->getContainerRegistryApi();
```



