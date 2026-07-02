# Certificates Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlcyUyRmNlcnRpZmljYXRlc19jcmVhdGU

To upload new SSL certificate which you have previously generated, send a POST
request to `/v2/certificates`.

When uploading a user-generated certificate, the `private_key`,
`leaf_certificate`, and optionally the `certificate_chain` attributes should
be provided. The type must be set to `custom`.

When using Let's Encrypt to create a certificate, the `dns_names` attribute
must be provided, and the type must be set to `lets_encrypt`.

```ruby
def certificates_create(body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [Let's Encrypt Certificate Request](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/let-s-encrypt-certificate-request.md) \| [Custom Certificate Request](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/custom-certificate-request.md) | Body, Required | This is a container for one-of cases. |


# Response Type

**201**: The response will be a JSON object with a key called `certificate`. The value of this will be an object that contains the standard attributes associated with a certificate.
When using Let's Encrypt, the initial value of the certificate's `state` attribute will be `pending`. When the certificate has been successfully issued by Let's Encrypt, this will transition to `verified` and be ready for use.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2CertificatesResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-certificates-response-1.md).


# Example Usage

```ruby
body = LetSEncryptCertificateRequest.new(
  name: 'web-cert-01',
  dns_names: [
    'www.example.com',
    'example.com'
  ],
  type: Type4::LETS_ENCRYPT
)

result = certificates_api.certificates_create(body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Example Response *(as JSON)*

```json
{
  "certificate": {
    "created_at": "2017-02-08T16:02:37Z",
    "dns_names": [
      ""
    ],
    "id": "892071a0-bb95-49bc-8021-3afd67a210bf",
    "name": "web-cert-01",
    "not_after": "2017-02-22T00:23:00Z",
    "sha1_fingerprint": "dfcc9f57d86bf58e321c2c6c31c7a971be244ac7",
    "state": "verified",
    "type": "custom"
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |



