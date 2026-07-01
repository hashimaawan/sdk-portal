# Get a Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlcyUyRkdldCUyNTIwYSUyNTIwQ2VydGlmaWNhdGU

Gets a specific Certificate object.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<CertificateResponse>> getACertificateAsync(
    final int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**200**: The `certificate` key contains a Certificate object

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CertificateResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/certificate-response.md).


# Example Usage

```java
int id = 112;

certificatesApi.getACertificateAsync(id).thenAccept(result -> {
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
  "certificate": {
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
}
```



