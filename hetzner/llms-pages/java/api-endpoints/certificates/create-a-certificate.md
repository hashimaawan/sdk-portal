# Create a Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlcyUyRkNyZWF0ZSUyNTIwYSUyNTIwQ2VydGlmaWNhdGU

Creates a new Certificate.

The default type **uploaded** allows for uploading your existing `certificate` and `private_key` in PEM format. You have to monitor its expiration date and handle renewal yourself.

In contrast, type **managed** requests a new Certificate from *Let's Encrypt* for the specified `domain_names`. Only domains managed by *Hetzner DNS* are supported. We handle renewal and timely alert the project owner via email if problems occur.

For type `managed` Certificates the `action` key of the response contains the Action that allows for tracking the issuance process. For type `uploaded` Certificates the `action` is always null.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<CreateCertificateResponse> createACertificateAsync(
    final CreateCertificateRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateCertificateRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/create-certificate-request.md) | Body, Optional | - |


# Response Type

**201**: The `certificate` key contains the Certificate that was just created. For type `managed` Certificates the `action` key contains the Action that allows for tracking the issuance process. For type `uploaded` Certificates the `action` is always null.

[`CreateCertificateResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/create-certificate-response.md)


# Example Usage

```java
CreateCertificateRequest body = new CreateCertificateRequest.Builder(
    "my website cert"
)
.domainNames(Arrays.asList(
        "example.com",
        "webmail.example.com",
        "www.example.com"
    ))
.type(Type1Enum.MANAGED)
.build();

certificatesController.createACertificateAsync(body).thenAccept(result -> {
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
  "action": {
    "command": "create_certificate",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 879,
        "type": "certificate"
      }
    ],
    "started": "2019-01-08T12:10:00+00:00",
    "status": "running"
  },
  "certificate": {
    "certificate": null,
    "created": "2019-01-08T12:10:00+00:00",
    "domain_names": [
      "example.com",
      "webmail.example.com",
      "www.example.com"
    ],
    "fingerprint": null,
    "id": 897,
    "labels": {
      "env": "dev"
    },
    "name": "my website cert",
    "not_valid_after": null,
    "not_valid_before": null,
    "status": {
      "error": null,
      "issuance": "pending",
      "renewal": "unavailable"
    },
    "type": "managed",
    "used_by": [
      {
        "id": 4711,
        "type": "load_balancer"
      }
    ]
  }
}
```



