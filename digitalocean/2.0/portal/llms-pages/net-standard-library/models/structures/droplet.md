# Droplet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRyb3BsZXQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Droplet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BackupIds` | `List<int>` | Required | An array of backup IDs of any backups that have been taken of the Droplet instance.  Droplet backups are enabled at the time of the instance creation. |
| `CreatedAt` | `DateTime` | Required | A time value given in ISO8601 combined date and time format that represents when the Droplet was created. |
| `Disk` | `int` | Required | The size of the Droplet's disk in gigabytes. |
| `Features` | `List<string>` | Required | An array of features enabled on this Droplet. |
| `Id` | `int` | Required | A unique identifier for each Droplet instance. This is automatically generated upon Droplet creation. |
| `Image` | [`Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/image-1.md) | Required | - |
| `Kernel` | [`Kernel`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/kernel.md) | Optional | **Note**: All Droplets created after March 2017 use internal kernels by default.<br>These Droplets will have this attribute set to `null`.<br><br>The current [kernel](https://www.digitalocean.com/docs/droplets/how-to/kernel/)<br>for Droplets with externally managed kernels. This will initially be set to<br>the kernel of the base image when the Droplet is created. |
| `Locked` | `bool` | Required | A boolean value indicating whether the Droplet has been locked, preventing actions by users. |
| `Memory` | `int` | Required | Memory of the Droplet in megabytes.<br><br>**Constraints**: *Multiple Of*: `8` |
| `Name` | `string` | Required | The human-readable name set for the Droplet instance. |
| `Networks` | [`Networks`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/networks.md) | Required | The details of the network that are configured for the Droplet instance.  This is an object that contains keys for IPv4 and IPv6.  The value of each of these is an array that contains objects describing an individual IP resource allocated to the Droplet.  These will define attributes like the IP address, netmask, and gateway of the specific network depending on the type of network it is. |
| `NextBackupWindow` | [`NextBackupWindow`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/next-backup-window.md) | Required | The details of the Droplet's backups feature, if backups are configured for the Droplet. This object contains keys for the start and end times of the window during which the backup will start. |
| `Region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/region.md) | Required | - |
| `Size` | [`Size`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/size.md) | Required | - |
| `SizeSlug` | `string` | Required | The unique slug identifier for the size of this Droplet. |
| `SnapshotIds` | `List<int>` | Required | An array of snapshot IDs of any snapshots created from the Droplet instance. |
| `Status` | [`Status8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/status-8.md) | Required | A status string indicating the state of the Droplet instance. This may be "new", "active", "off", or "archive". |
| `Tags` | `List<string>` | Required | An array of Tags the Droplet has been tagged with. |
| `Vcpus` | `int` | Required | The number of virtual CPUs. |
| `VolumeIds` | `List<string>` | Required | A flat array including the unique identifier for each Block Storage volume attached to the Droplet. |
| `VpcUuid` | `string` | Optional | A string specifying the UUID of the VPC to which the Droplet is assigned. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

Droplet droplet = new Droplet
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
        Description = "description6",
        Distribution = Distribution.Ubuntu,
        ErrorMessage = "error_message8",
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
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Locked = false,
    Memory = 1024,
    Name = "example.com",
    Networks = new Networks
    {
        V4 = new List<V4>
        {
            new V4
            {
                Gateway = "gateway2",
                IpAddress = "ip_address2",
                Netmask = "netmask2",
                Type = Type10.Public,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new V4
            {
                Gateway = "gateway2",
                IpAddress = "ip_address2",
                Netmask = "netmask2",
                Type = Type10.Public,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new V4
            {
                Gateway = "gateway2",
                IpAddress = "ip_address2",
                Netmask = "netmask2",
                Type = Type10.Public,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        V6 = new List<V6>
        {
            new V6
            {
                Gateway = "gateway4",
                IpAddress = "ip_address4",
                Netmask = 106,
                Type = Type11.Public,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new V6
            {
                Gateway = "gateway4",
                IpAddress = "ip_address4",
                Netmask = 106,
                Type = Type11.Public,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    NextBackupWindow = new NextBackupWindow
    {
        End = DateTime.ParseExact("2019-12-04T23:00:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        Start = DateTime.ParseExact("2019-12-04T00:00:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
    Kernel = new Kernel
    {
        Id = 16,
        Name = "name4",
        Version = "version0",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    VpcUuid = "760e09ef-dc84-11e8-981e-3cfdfeaae000",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



