# Floating Ip 1 Droplet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkZsb2F0aW5nSXAxRHJvcGxldA


# Class Name

`FloatingIp1Droplet`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | models.FloatingIp1DropletContainer.FromObject(interface{} object) |
| [`models.Droplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/droplet.md) | models.FloatingIp1DropletContainer.FromDroplet(models.Droplet droplet) |


# interface{}

## Initialization Code

### Example

```go
value := models.FloatingIp1DropletContainer.FromObject(interface{}("[key1, val1][key2, val2]"))
```


# models.Droplet

## Initialization Code

### Example

```go
value := models.FloatingIp1DropletContainer.FromDroplet(models.Droplet{
    BackupIds:             []int{
        53893572,
    },
    CreatedAt:             parseTime(time.RFC3339, "2020-07-21T18:37:44Z", func(err error) { log.Fatalln(err) }),
    Disk:                  25,
    Features:              []string{
        "backups",
        "private_networking",
        "ipv6",
    },
    Id:                    3164444,
    Image:                 models.Image1{
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-05-04T22:23:02Z", func(err error) { log.Fatalln(err) })),
        Distribution:          models.ToPointer(models.Distribution_Ubuntu),
        Id:                    models.ToPointer(7555620),
        MinDiskSize:           models.NewOptional(models.ToPointer(20)),
        Name:                  models.ToPointer("Nifty New Snapshot"),
        Public:                models.ToPointer(true),
        Regions:               []models.Region2{
            models.Region2_Nyc1,
            models.Region2_Nyc2,
        },
        SizeGigabytes:         models.NewOptional(models.ToPointer(float64(2.34))),
        Slug:                  models.NewOptional(models.ToPointer("nifty1")),
        Status:                models.ToPointer(models.Status7_New),
        Tags:                  models.NewOptional(models.ToPointer([]string{
            "base-image",
            "prod",
        })),
        Type:                  models.ToPointer(models.Type9_Snapshot),
    },
    Locked:                false,
    Memory:                1024,
    Name:                  "example.com",
    Networks:              models.Networks{
    },
    NextBackupWindow:      models.ToPointer(models.NextBackupWindow{
        End:                   models.ToPointer(parseTime(time.RFC3339, "2019-12-04T23:00:00Z", func(err error) { log.Fatalln(err) })),
        Start:                 models.ToPointer(parseTime(time.RFC3339, "2019-12-04T00:00:00Z", func(err error) { log.Fatalln(err) })),
    }),
    Region:                models.Region{
        Available:             true,
        Features:              []string{
            "private_networking",
            "backups",
            "ipv6",
            "metadata",
            "install_agent",
            "storage",
            "image_transfer",
        },
        Name:                  "New York 3",
        Sizes:                 []string{
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
        Slug:                  "nyc3",
    },
    Size:                  models.Size{
        Available:             true,
        Description:           "Basic",
        Disk:                  25,
        Memory:                1024,
        PriceHourly:           float64(0.00743999984115362),
        PriceMonthly:          float64(5),
        Regions:               []string{
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
        Slug:                  "s-1vcpu-1gb",
        Transfer:              float64(1),
        Vcpus:                 1,
    },
    SizeSlug:              "s-1vcpu-1gb",
    SnapshotIds:           []int{
        67512819,
    },
    Status:                models.Status8_Active,
    Tags:                  []string{
        "web",
        "env:prod",
    },
    Vcpus:                 1,
    VolumeIds:             []string{
        "506f78a4-e098-11e5-ad9f-000f53306ae1",
    },
    VpcUuid:               models.ToPointer("760e09ef-dc84-11e8-981e-3cfdfeaae000"),
})
```



