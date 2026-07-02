# Kubernetes List Options

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkt1YmVybmV0ZXMlMkZrdWJlcm5ldGVzX2xpc3Rfb3B0aW9ucw

To list the versions of Kubernetes available for use, the regions that support Kubernetes, and the available node sizes, send a GET request to `/v2/kubernetes/options`.

```go
KubernetesListOptions(
    ctx context.Context) (
    models.ApiResponse[models.V2KubernetesOptionsResponse],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Response Type

**200**: The response will be a JSON object with a key called `options` which contains
`regions`, `versions`, and `sizes` objects listing the available options and
the matching slugs for use when creating a new cluster.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2KubernetesOptionsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-kubernetes-options-response.md).


# Example Usage

```go
ctx := context.Background()

apiResponse, err := kubernetesApi.KubernetesListOptions(ctx)
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
  "options": {
    "regions": [
      {
        "name": "New York 1",
        "slug": "nyc1"
      },
      {
        "name": "Singapore 1",
        "slug": "sgp1"
      },
      {
        "name": "London 1",
        "slug": "lon1"
      },
      {
        "name": "New York 3",
        "slug": "nyc3"
      },
      {
        "name": "Amsterdam 3",
        "slug": "ams3"
      },
      {
        "name": "Frankfurt 1",
        "slug": "fra1"
      },
      {
        "name": "Toronto 1",
        "slug": "tor1"
      },
      {
        "name": "San Francisco 2",
        "slug": "sfo2"
      },
      {
        "name": "Bangalore 1",
        "slug": "blr1"
      },
      {
        "name": "San Francisco 3",
        "slug": "sfo3"
      }
    ],
    "sizes": [
      {
        "name": "s-1vcpu-2gb",
        "slug": "s-1vcpu-2gb"
      },
      {
        "name": "s-2vcpu-2gb",
        "slug": "s-2vcpu-2gb"
      },
      {
        "name": "s-1vcpu-3gb",
        "slug": "s-1vcpu-3gb"
      },
      {
        "name": "s-2vcpu-4gb",
        "slug": "s-2vcpu-4gb"
      },
      {
        "name": "s-4vcpu-8gb",
        "slug": "s-4vcpu-8gb"
      },
      {
        "name": "c-2-4GiB",
        "slug": "c-2"
      },
      {
        "name": "g-2vcpu-8gb",
        "slug": "g-2vcpu-8gb"
      },
      {
        "name": "gd-2vcpu-8gb",
        "slug": "gd-2vcpu-8gb"
      },
      {
        "name": "s-8vcpu-16gb",
        "slug": "s-8vcpu-16gb"
      },
      {
        "name": "s-6vcpu-16gb",
        "slug": "s-6vcpu-16gb"
      },
      {
        "name": "c-4-8GiB",
        "slug": "c-4"
      },
      {
        "name": "m-2vcpu-16gb",
        "slug": "m-2vcpu-16gb"
      },
      {
        "name": "m3-2vcpu-16gb",
        "slug": "m3-2vcpu-16gb"
      },
      {
        "name": "g-4vcpu-16gb",
        "slug": "g-4vcpu-16gb"
      },
      {
        "name": "gd-4vcpu-16gb",
        "slug": "gd-4vcpu-16gb"
      },
      {
        "name": "m6-2vcpu-16gb",
        "slug": "m6-2vcpu-16gb"
      },
      {
        "name": "s-8vcpu-32gb",
        "slug": "s-8vcpu-32gb"
      },
      {
        "name": "c-8-16GiB",
        "slug": "c-8"
      },
      {
        "name": "m-4vcpu-32gb",
        "slug": "m-4vcpu-32gb"
      },
      {
        "name": "m3-4vcpu-32gb",
        "slug": "m3-4vcpu-32gb"
      },
      {
        "name": "g-8vcpu-32gb",
        "slug": "g-8vcpu-32gb"
      },
      {
        "name": "s-12vcpu-48gb",
        "slug": "s-12vcpu-48gb"
      },
      {
        "name": "gd-8vcpu-32gb",
        "slug": "gd-8vcpu-32gb"
      },
      {
        "name": "m6-4vcpu-32gb",
        "slug": "m6-4vcpu-32gb"
      },
      {
        "name": "s-16vcpu-64gb",
        "slug": "s-16vcpu-64gb"
      },
      {
        "name": "c-16",
        "slug": "c-16"
      },
      {
        "name": "m-8vcpu-64gb",
        "slug": "m-8vcpu-64gb"
      },
      {
        "name": "m3-8vcpu-64gb",
        "slug": "m3-8vcpu-64gb"
      },
      {
        "name": "g-16vcpu-64gb",
        "slug": "g-16vcpu-64gb"
      },
      {
        "name": "s-20vcpu-96gb",
        "slug": "s-20vcpu-96gb"
      },
      {
        "name": "gd-16vcpu-64gb",
        "slug": "gd-16vcpu-64gb"
      },
      {
        "name": "m6-8vcpu-64gb",
        "slug": "m6-8vcpu-64gb"
      },
      {
        "name": "s-24vcpu-128gb",
        "slug": "s-24vcpu-128gb"
      },
      {
        "name": "c-32-64GiB",
        "slug": "c-32"
      },
      {
        "name": "m-16vcpu-128gb",
        "slug": "m-16vcpu-128gb"
      },
      {
        "name": "m3-16vcpu-128gb",
        "slug": "m3-16vcpu-128gb"
      },
      {
        "name": "g-32vcpu-128gb",
        "slug": "g-32vcpu-128gb"
      },
      {
        "name": "s-32vcpu-192gb",
        "slug": "s-32vcpu-192gb"
      },
      {
        "name": "gd-32vcpu-128gb",
        "slug": "gd-32vcpu-128gb"
      },
      {
        "name": "m-24vcpu-192gb",
        "slug": "m-24vcpu-192gb"
      },
      {
        "name": "m6-16vcpu-128gb",
        "slug": "m6-16vcpu-128gb"
      },
      {
        "name": "g-40vcpu-160gb",
        "slug": "g-40vcpu-160gb"
      },
      {
        "name": "gd-40vcpu-160gb",
        "slug": "gd-40vcpu-160gb"
      },
      {
        "name": "m3-24vcpu-192gb",
        "slug": "m3-24vcpu-192gb"
      },
      {
        "name": "m-32vcpu-256gb",
        "slug": "m-32vcpu-256gb"
      },
      {
        "name": "m6-24vcpu-192gb",
        "slug": "m6-24vcpu-192gb"
      },
      {
        "name": "m3-32vcpu-256gb",
        "slug": "m3-32vcpu-256gb"
      },
      {
        "name": "m6-32vcpu-256gb",
        "slug": "m6-32vcpu-256gb"
      }
    ],
    "versions": [
      {
        "kubernetes_version": "1.18.8",
        "slug": "1.18.8-do.0",
        "supported_features": [
          "cluster-autoscaler",
          "docr-integration",
          "token-authentication"
        ]
      },
      {
        "kubernetes_version": "1.17.11",
        "slug": "1.17.11-do.0",
        "supported_features": [
          "cluster-autoscaler",
          "docr-integration",
          "token-authentication"
        ]
      },
      {
        "kubernetes_version": "1.16.14",
        "slug": "1.16.14-do.0",
        "supported_features": [
          "cluster-autoscaler",
          "docr-integration",
          "token-authentication"
        ]
      }
    ]
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



