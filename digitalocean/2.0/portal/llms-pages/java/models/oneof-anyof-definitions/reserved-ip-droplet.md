# Reserved Ip Droplet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlc2VydmVkSXBEcm9wbGV0


# Class Name

`ReservedIpDroplet`


# Cases

| Type | Factory Method |
|  --- | --- |
| `Object` | ReservedIpDroplet.fromObject(Object object) |
| [`Droplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/droplet.md) | ReservedIpDroplet.fromDroplet(Droplet droplet) |


# Object

## Initialization Code

### Example

```java
ReservedIpDroplet.fromObject(
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
    )
```


# Droplet

## Initialization Code

### Example

```java
ReservedIpDroplet.fromDroplet(
        new Droplet.Builder(
            Arrays.asList(
                53893572
            ),
            DateTimeHelper.fromRfc8601DateTime("2020-07-21T18:37:44Z"),
            25,
            Arrays.asList(
                "backups",
                "private_networking",
                "ipv6"
            ),
            3164444,
            new Image1.Builder()
                .createdAt(DateTimeHelper.fromRfc8601DateTime("2020-05-04T22:23:02Z"))
                .distribution(Distribution.UBUNTU)
                .id(7555620)
                .minDiskSize(20)
                .name("Nifty New Snapshot")
                .mPublic(true)
                .regions(Arrays.asList(
                    Region2.NYC1,
                    Region2.NYC2
                ))
                .sizeGigabytes(2.34D)
                .slug("nifty1")
                .status(Status7.NEW)
                .tags(Arrays.asList(
                    "base-image",
                    "prod"
                ))
                .type(Type9.SNAPSHOT)
                .build(),
            false,
            1024,
            "example.com",
            new Networks.Builder()
                .build(),
            new NextBackupWindow.Builder()
                .end(DateTimeHelper.fromRfc8601DateTime("2019-12-04T23:00:00Z"))
                .start(DateTimeHelper.fromRfc8601DateTime("2019-12-04T00:00:00Z"))
                .build(),
            new Region.Builder(
                true,
                Arrays.asList(
                    "private_networking",
                    "backups",
                    "ipv6",
                    "metadata",
                    "install_agent",
                    "storage",
                    "image_transfer"
                ),
                "New York 3",
                Arrays.asList(
                    "s-1vcpu-1gb",
                    "s-1vcpu-2gb",
                    "s-1vcpu-3gb",
                    "s-2vcpu-2gb",
                    "s-3vcpu-1gb",
                    "s-2vcpu-4gb",
                    "s-4vcpu-8gb",
                    "s-6vcpu-16gb",
                    "s-8vcpu-32gb",
                    "s-12vcpu-48gb",
                    "s-16vcpu-64gb",
                    "s-20vcpu-96gb",
                    "s-24vcpu-128gb",
                    "s-32vcpu-192g"
                ),
                "nyc3"
            )
            .build(),
            new Size.Builder(
                true,
                "Basic",
                25,
                1024,
                0.00743999984115362D,
                5D,
                Arrays.asList(
                    "ams2",
                    "ams3",
                    "blr1",
                    "fra1",
                    "lon1",
                    "nyc1",
                    "nyc2",
                    "nyc3",
                    "sfo1",
                    "sfo2",
                    "sfo3",
                    "sgp1",
                    "tor1"
                ),
                "s-1vcpu-1gb",
                1D,
                1
            )
            .build(),
            "s-1vcpu-1gb",
            Arrays.asList(
                67512819
            ),
            Status8.ACTIVE,
            Arrays.asList(
                "web",
                "env:prod"
            ),
            1,
            Arrays.asList(
                "506f78a4-e098-11e5-ad9f-000f53306ae1"
            )
        )
        .vpcUuid("760e09ef-dc84-11e8-981e-3cfdfeaae000")
        .build()
    )
```



