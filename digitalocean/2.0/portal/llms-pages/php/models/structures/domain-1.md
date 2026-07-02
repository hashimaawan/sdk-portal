# Domain 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRvbWFpbjE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Domain1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ipAddress` | `?string` | Optional | This optional attribute may contain an IP address. When provided, an A record will be automatically created pointing to the apex domain. | getIpAddress(): ?string | setIpAddress(?string ipAddress): void |
| `name` | `?string` | Optional | The name of the domain itself. This should follow the standard domain format of domain.TLD. For instance, `example.com` is a valid domain name. | getName(): ?string | setName(?string name): void |
| `ttl` | `?int` | Optional, Read-only | This value is the time to live for the records on this domain, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. | getTtl(): ?int | setTtl(?int ttl): void |
| `zoneFile` | `?string` | Optional, Read-only | This attribute contains the complete contents of the zone file for the selected domain. Individual domain record resources should be used to get more granular control over records. However, this attribute can also be used to get information about the SOA record, which is created automatically and is not accessible as an individual record resource. | getZoneFile(): ?string | setZoneFile(?string zoneFile): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Domain1Builder;
use DigitalOceanApiLib\ApiHelper;

$domain1 = Domain1Builder::init()
    ->ipAddress('192.0.2.1')
    ->name('example.com')
    ->ttl(1800)
    ->zoneFile('$ORIGIN example.com.
$TTL 1800
example.com. IN SOA ns1.digitalocean.com. hostmaster.example.com. 1415982609 10800 3600 604800 1800
example.com. 1800 IN NS ns1.digitalocean.com.
example.com. 1800 IN NS ns2.digitalocean.com.
example.com. 1800 IN NS ns3.digitalocean.com.
example.com. 1800 IN A 1.2.3.4
')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



