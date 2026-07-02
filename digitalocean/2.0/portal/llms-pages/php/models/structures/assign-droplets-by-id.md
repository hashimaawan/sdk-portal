# Assign Droplets by ID

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkFzc2lnbiUyNTIwRHJvcGxldHMlMjUyMGJ5JTI1MjBJRA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`AssignDropletsById`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dropletIds` | `int[]` | Required | An array containing the IDs of the Droplets assigned to the load balancer. | getDropletIds(): array | setDropletIds(array dropletIds): void |
| `region` | [`string(Region2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. | getRegion(): string | setRegion(string region): void |
| `algorithm` | [`?string(Algorithm)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/algorithm.md) | Optional | This field has been deprecated. You can no longer specify an algorithm for load balancers.<br><br>**Default**: `Algorithm::ROUND_ROBIN` | getAlgorithm(): ?string | setAlgorithm(?string algorithm): void |
| `createdAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the load balancer was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `disableLetsEncryptDnsRecords` | `?bool` | Optional | A boolean value indicating whether to disable automatic DNS record creation for Let's Encrypt certificates that are added to the load balancer.<br><br>**Default**: `false` | getDisableLetsEncryptDnsRecords(): ?bool | setDisableLetsEncryptDnsRecords(?bool disableLetsEncryptDnsRecords): void |
| `enableBackendKeepalive` | `?bool` | Optional | A boolean value indicating whether HTTP keepalive connections are maintained to target Droplets.<br><br>**Default**: `false` | getEnableBackendKeepalive(): ?bool | setEnableBackendKeepalive(?bool enableBackendKeepalive): void |
| `enableProxyProtocol` | `?bool` | Optional | A boolean value indicating whether PROXY Protocol is in use.<br><br>**Default**: `false` | getEnableProxyProtocol(): ?bool | setEnableProxyProtocol(?bool enableProxyProtocol): void |
| `firewall` | [`?Firewall1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/firewall-1.md) | Optional | An object specifying allow and deny rules to control traffic to the load balancer. | getFirewall(): ?Firewall1 | setFirewall(?Firewall1 firewall): void |
| `forwardingRules` | [`ForwardingRule[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/forwarding-rule.md) | Required | An array of objects specifying the forwarding rules for a load balancer.<br><br>**Constraints**: *Minimum Items*: `1` | getForwardingRules(): array | setForwardingRules(array forwardingRules): void |
| `healthCheck` | [`?HealthCheck1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/health-check-1.md) | Optional | An object specifying health check settings for the load balancer. | getHealthCheck(): ?HealthCheck1 | setHealthCheck(?HealthCheck1 healthCheck): void |
| `httpIdleTimeoutSeconds` | `?int` | Optional | An integer value which configures the idle timeout for HTTP requests to the target droplets.<br><br>**Default**: `60`<br><br>**Constraints**: `>= 30`, `<= 600` | getHttpIdleTimeoutSeconds(): ?int | setHttpIdleTimeoutSeconds(?int httpIdleTimeoutSeconds): void |
| `id` | `?string` | Optional, Read-only | A unique ID that can be used to identify and reference a load balancer. | getId(): ?string | setId(?string id): void |
| `ip` | `?string` | Optional, Read-only | An attribute containing the public-facing IP address of the load balancer.<br><br>**Constraints**: *Pattern*: `^$\|^((25[0-5]\|2[0-4][0-9]\|[01]?[0-9][0-9]?)\.){3}(25[0-5]\|2[0-4][0-9]\|[01]?[0-9][0-9]?)$` | getIp(): ?string | setIp(?string ip): void |
| `name` | `?string` | Optional | A human-readable name for a load balancer instance. | getName(): ?string | setName(?string name): void |
| `projectId` | `?string` | Optional | The ID of the project that the load balancer is associated with. If no ID is provided at creation, the load balancer associates with the user's default project. If an invalid project ID is provided, the load balancer will not be created. | getProjectId(): ?string | setProjectId(?string projectId): void |
| `redirectHttpToHttps` | `?bool` | Optional | A boolean value indicating whether HTTP requests to the load balancer on port 80 will be redirected to HTTPS on port 443.<br><br>**Default**: `false` | getRedirectHttpToHttps(): ?bool | setRedirectHttpToHttps(?bool redirectHttpToHttps): void |
| `size` | [`?string(Size2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/size-2.md) | Optional | This field has been replaced by the `size_unit` field for all regions except in AMS2, NYC2, and SFO1. Each available load balancer size now equates to the load balancer having a set number of nodes.<br><br>* `lb-small` = 1 node<br>* `lb-medium` = 3 nodes<br>* `lb-large` = 6 nodes<br><br>You can resize load balancers after creation up to once per hour. You cannot resize a load balancer within the first hour of its creation.<br><br>**Default**: `Size2::LBSMALL` | getSize(): ?string | setSize(?string size): void |
| `sizeUnit` | `?int` | Optional | How many nodes the load balancer contains. Each additional node increases the load balancer's ability to manage more connections. Load balancers can be scaled up or down, and you can change the number of nodes after creation up to once per hour. This field is currently not available in the AMS2, NYC2, or SFO1 regions. Use the `size` field to scale load balancers that reside in these regions.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1`, `<= 100` | getSizeUnit(): ?int | setSizeUnit(?int sizeUnit): void |
| `status` | [`?string(Status12)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-12.md) | Optional, Read-only | A status string indicating the current state of the load balancer. This can be `new`, `active`, or `errored`. | getStatus(): ?string | setStatus(?string status): void |
| `stickySessions` | [`?StickySessions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/sticky-sessions.md) | Optional | An object specifying sticky sessions settings for the load balancer. | getStickySessions(): ?StickySessions | setStickySessions(?StickySessions stickySessions): void |
| `vpcUuid` | `?string` | Optional | A string specifying the UUID of the VPC to which the load balancer is assigned. | getVpcUuid(): ?string | setVpcUuid(?string vpcUuid): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\AssignDropletsByIdBuilder;
use DigitalOceanApiLib\Models\Region2;
use DigitalOceanApiLib\Models\Builders\ForwardingRuleBuilder;
use DigitalOceanApiLib\Models\EntryProtocol;
use DigitalOceanApiLib\Models\TargetProtocol;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Algorithm;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Size2;
use DigitalOceanApiLib\Models\Status12;

$assignDropletsById = AssignDropletsByIdBuilder::init(
    [
        3164444,
        3164445
    ],
    Region2::NYC3,
    [
        ForwardingRuleBuilder::init(
            443,
            EntryProtocol::HTTPS,
            80,
            TargetProtocol::HTTP
        )
            ->certificateId('892071a0-bb95-49bc-8021-3afd67a210bf')
            ->tlsPassthrough(false)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->algorithm(Algorithm::ROUND_ROBIN)
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2017-02-01T22:22:58Z'))
    ->disableLetsEncryptDnsRecords(true)
    ->enableBackendKeepalive(true)
    ->enableProxyProtocol(true)
    ->httpIdleTimeoutSeconds(90)
    ->id('4de7ac8b-495b-4884-9a69-1050c6793cd6')
    ->ip('104.131.186.241')
    ->name('example-lb-01')
    ->projectId('4de7ac8b-495b-4884-9a69-1050c6793cd6')
    ->redirectHttpToHttps(true)
    ->size(Size2::LBSMALL)
    ->sizeUnit(3)
    ->status(Status12::NEW_)
    ->vpcUuid('c33931f2-a26a-4e61-b85c-4e95a2ec431b')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



