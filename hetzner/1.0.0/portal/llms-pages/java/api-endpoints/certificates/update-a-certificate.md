# Update a Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlcyUyRlVwZGF0ZSUyNTIwYSUyNTIwQ2VydGlmaWNhdGU

Updates the Certificate properties.

Note that when updating labels, the Certificate’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

Note: if the Certificate object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<CertificateResponse>> updateACertificateAsync(
    final int id,
    final UpdateCertificateRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |
| `body` | [`UpdateCertificateRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/update-certificate-request.md) | Body, Optional | - |


# Response Type

**200**: The `certificate` key contains the Certificate that was just updated

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CertificateResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/certificate-response.md).


# Example Usage

```java
int id = 112;
UpdateCertificateRequest body = new UpdateCertificateRequest.Builder()
    .labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
    .name("my website cert")
    .build();

certificatesApi.updateACertificateAsync(id, body).thenAccept(result -> {
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
      "labelkey": "value"
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



