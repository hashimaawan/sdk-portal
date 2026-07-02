# Floating Ip 1 Droplet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nSXAxRHJvcGxldA


# Class Name

`FloatingIp1Droplet`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`object`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | FloatingIp1Droplet.FromObject(object mObject) |
| [`Droplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/droplet.md) | FloatingIp1Droplet.FromDroplet(Droplet droplet) |


# object

## Initialization Code

### Example

```csharp
FloatingIp1Droplet value = FloatingIp1Droplet.FromObject(
    ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}")
);
```


# Droplet

## Initialization Code

### Example

```csharp
FloatingIp1Droplet value = FloatingIp1Droplet.FromDroplet(
    new Droplet
    {
        BackupIds = new List<int>
        {
            53893572,
        },
        CreatedAt = DateTime.ParseExact("2020-07-21T18:37:44Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        Disk = 25,
        Features = new List<string>
        {
            "backups",
            "private_networking",
            "ipv6",
        },
        Id = 3164444,
        Image = new Image1
        {
            CreatedAt = DateTime.ParseExact("2020-05-04T22:23:02Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Distribution = Distribution.Ubuntu,
            Id = 7555620,
            MinDiskSize = 20,
            Name = "Nifty New Snapshot",
            MPublic = true,
            Regions = new List<Region2>
            {
                Region2.Nyc1,
                Region2.Nyc2,
            },
            SizeGigabytes = 2.34,
            Slug = "nifty1",
            Status = Status7.New,
            Tags = new List<string>
            {
                "base-image",
                "prod",
            },
            Type = Type9.Snapshot,
        },
        Locked = false,
        Memory = 1024,
        Name = "example.com",
        Networks = new Networks
        {
        },
        NextBackupWindow = new NextBackupWindow
        {
            End = DateTime.ParseExact("2019-12-04T23:00:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Start = DateTime.ParseExact("2019-12-04T00:00:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
        },
        Region = new Region
        {
            Available = true,
            Features = new List<string>
            {
                "private_networking",
                "backups",
                "ipv6",
                "metadata",
                "install_agent",
                "storage",
                "image_transfer",
            },
            Name = "New York 3",
            Sizes = new List<string>
            {
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
                "s-32vcpu-192g",
            },
            Slug = "nyc3",
        },
        Size = new Size
        {
            Available = true,
            Description = "Basic",
            Disk = 25,
            Memory = 1024,
            PriceHourly = 0.00743999984115362,
            PriceMonthly = 5,
            Regions = new List<string>
            {
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
                "tor1",
            },
            Slug = "s-1vcpu-1gb",
            Transfer = 1,
            Vcpus = 1,
        },
        SizeSlug = "s-1vcpu-1gb",
        SnapshotIds = new List<int>
        {
            67512819,
        },
        Status = Status8.Active,
        Tags = new List<string>
        {
            "web",
            "env:prod",
        },
        Vcpus = 1,
        VolumeIds = new List<string>
        {
            "506f78a4-e098-11e5-ad9f-000f53306ae1",
        },
        VpcUuid = "760e09ef-dc84-11e8-981e-3cfdfeaae000",
    }
);
```



