# Create a Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlcyUyRkNyZWF0ZSUyNTIwYSUyNTIwQ2VydGlmaWNhdGU

Creates a new Certificate.

The default type **uploaded** allows for uploading your existing `certificate` and `private_key` in PEM format. You have to monitor its expiration date and handle renewal yourself.

In contrast, type **managed** requests a new Certificate from *Let's Encrypt* for the specified `domain_names`. Only domains managed by *Hetzner DNS* are supported. We handle renewal and timely alert the project owner via email if problems occur.

For type `managed` Certificates the `action` key of the response contains the Action that allows for tracking the issuance process. For type `uploaded` Certificates the `action` is always null.

:information_source: **Note** This endpoint does not require authentication.

```python
def create_a_certificate(self,
                        body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateCertificateRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/create-certificate-request.md) | Body, Optional | - |


# Response Type

**201**: The `certificate` key contains the Certificate that was just created. For type `managed` Certificates the `action` key contains the Action that allows for tracking the issuance process. For type `uploaded` Certificates the `action` is always null.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`CreateCertificateResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/create-certificate-response.md).


# Example Usage

```python
body = CreateCertificateRequest(
    name='my website cert',
    domain_names=[
        'example.com',
        'webmail.example.com',
        'www.example.com'
    ],
    mtype=Type1.MANAGED
)

result = certificates_api.create_a_certificate(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
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



