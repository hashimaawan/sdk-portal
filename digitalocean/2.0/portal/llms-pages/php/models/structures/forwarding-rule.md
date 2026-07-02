# Forwarding Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkZvcndhcmRpbmdSdWxl

An object specifying a forwarding rule for a load balancer.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`ForwardingRule`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificateId` | `?string` | Optional | The ID of the TLS certificate used for SSL termination if enabled. | getCertificateId(): ?string | setCertificateId(?string certificateId): void |
| `entryPort` | `int` | Required | An integer representing the port on which the load balancer instance will listen. | getEntryPort(): int | setEntryPort(int entryPort): void |
| `entryProtocol` | [`string(EntryProtocol)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/entry-protocol.md) | Required | The protocol used for traffic to the load balancer. The possible values are: `http`, `https`, `http2`, `http3`, `tcp`, or `udp`. If you set the  `entry_protocol` to `udp`, the `target_protocol` must be set to `udp`.  When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly. | getEntryProtocol(): string | setEntryProtocol(string entryProtocol): void |
| `targetPort` | `int` | Required | An integer representing the port on the backend Droplets to which the load balancer will send traffic. | getTargetPort(): int | setTargetPort(int targetPort): void |
| `targetProtocol` | [`string(TargetProtocol)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/target-protocol.md) | Required | The protocol used for traffic from the load balancer to the backend Droplets. The possible values are: `http`, `https`, `http2`, `tcp`, or `udp`. If you set the `target_protocol` to `udp`, the `entry_protocol` must be set to  `udp`. When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly. | getTargetProtocol(): string | setTargetProtocol(string targetProtocol): void |
| `tlsPassthrough` | `?bool` | Optional | A boolean value indicating whether SSL encrypted traffic will be passed through to the backend Droplets. | getTlsPassthrough(): ?bool | setTlsPassthrough(?bool tlsPassthrough): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ForwardingRuleBuilder;
use DigitalOceanApiLib\Models\EntryProtocol;
use DigitalOceanApiLib\Models\TargetProtocol;
use DigitalOceanApiLib\ApiHelper;

$forwardingRule = ForwardingRuleBuilder::init(
    443,
    EntryProtocol::HTTPS,
    80,
    TargetProtocol::HTTP
)
    ->certificateId('892071a0-bb95-49bc-8021-3afd67a210bf')
    ->tlsPassthrough(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



