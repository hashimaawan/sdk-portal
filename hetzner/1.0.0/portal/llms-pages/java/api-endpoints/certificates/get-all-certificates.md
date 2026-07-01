# Get All Certificates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlcyUyRkdldCUyNTIwYWxsJTI1MjBDZXJ0aWZpY2F0ZXM

Returns all Certificate objects.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<CertificatesResponse>> getAllCertificatesAsync(
    final Sort sort,
    final String name,
    final String labelSelector,
    final ParameterType type)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `type` | [`ParameterType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/parameter-type.md) | Query, Optional | Can be used multiple times. The response will only contain Certificates matching the type. |


# Response Type

**200**: The `certificates` key contains an array of Certificate objects

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CertificatesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/certificates-response.md).


# Example Usage

```java
certificatesApi.getAllCertificatesAsync(null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Example Response *(as JSON)*

```json
{
  "certificates": [
    {
      "certificate": "-----BEGIN CERTIFICATE-----\n...",
      "created": "2019-01-08T12:10:00+00:00",
      "domain_names": [
        "example.com",
        "webmail.example.com",
        "www.example.com"
      ],
      "fingerprint": "03:c7:55:9b:2a:d1:04:17:09:f6:d0:7f:18:34:63:d4:3e:5f",
      "id": 897,
      "labels": {
        "env": "dev"
      },
      "name": "my website cert",
      "not_valid_after": "2019-07-08T09:59:59+00:00",
      "not_valid_before": "2019-01-08T10:00:00+00:00",
      "status": null,
      "type": "uploaded",
      "used_by": [
        {
          "id": 4711,
          "type": "load_balancer"
        }
      ]
    }
  ]
}
```



