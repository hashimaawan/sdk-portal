# Create a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZDcmVhdGUlMjUyMGElMjUyMFNlcnZlcg

Creates a new Server. Returns preliminary information about the Server as well as an Action that covers progress of creation.

:information_source: **Note** This endpoint does not require authentication.

```php
function createAServer(?CreateServerRequest $body = null): CreateServerResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`?CreateServerRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/create-server-request.md) | Body, Optional | Please note that Server names must be unique per Project and valid hostnames as per RFC 1123 (i.e. may only contain letters, digits, periods, and dashes).<br><br>For `server_type` you can either use the ID as listed in `/server_types` or its name.<br><br>For `image` you can either use the ID as listed in `/images` or its name.<br><br>If you want to create the Server in a Location, you must set `location` to the ID or name as listed in `/locations`. This is the recommended way. You can be even more specific by setting `datacenter` to the ID or name as listed in `/datacenters`. However we only recommend this if you want to assign a specific Primary IP to the Server which is located in the specified Datacenter.<br><br>Some properties like `start_after_create` or `automount` will trigger Actions after the Server is created. Those Actions are listed in the `next_actions` field in the response.<br><br>For accessing your Server we strongly recommend to use SSH keys by passing the respective key IDs in `ssh_keys`. If you do not specify any `ssh_keys` we will generate a root password for you and return it in the response.<br><br>Please note that provided user-data is stored in our systems. While we take measures to protect it we highly recommend that you don’t use it to store passwords or other sensitive information.<br><br>#### Call specific error codes<br><br>\| Code                             \| Description                                                \|<br>\|----------------------------------\|------------------------------------------------------------\|<br>\| `placement_error`                \| An error during the placement occurred                     \|<br>\| `primary_ip_assigned`            \| The specified Primary IP is already assigned to a server   \|<br>\| `primary_ip_datacenter_mismatch` \| The specified Primary IP is in a different datacenter      \|<br>\| `primary_ip_version_mismatch`    \| The specified Primary IP has the wrong IP Version          \| |


# Response Type

**201**: The `server` key in the reply contains a Server object with this structure

[`CreateServerResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/create-server-response.md)


# Example Usage

```php
$body = CreateServerRequestBuilder::init(
    'ubuntu-20.04',
    'my-server',
    'cx11'
)
    ->automount(false)
    ->datacenter('nbg1-dc3')
    ->firewalls(
        [
            Firewall4Builder::init()
                ->firewall(38)
                ->build()
        ]
    )
    ->location('nbg1')
    ->networks(
        [
            456
        ]
    )
    ->placementGroup(1)
    ->sshKeys(
        [
            'my-ssh-key'
        ]
    )
    ->startAfterCreate(true)
    ->userData('#cloud-config
runcmd:
- [touch, /root/cloud-init-worked]
')
    ->volumes(
        [
            123
        ]
    )
    ->build();

$serversController = $client->getServersController();

try {
    $result = $serversController->createAServer($body);
    echo 'CreateServerResponse:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "create_server",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 1,
    "progress": 0,
    "resources": [
      {
        "id": 42,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  },
  "next_actions": [
    {
      "command": "start_server",
      "error": {
        "code": "action_failed",
        "message": "Action failed"
      },
      "finished": null,
      "id": 13,
      "progress": 0,
      "resources": [
        {
          "id": 42,
          "type": "server"
        }
      ],
      "started": "2016-01-30T23:50:00+00:00",
      "status": "running"
    }
  ],
  "root_password": "YItygq1v3GYjjMomLaKc",
  "server": {
    "backup_window": "22-02",
    "created": "2016-01-30T23:50:00+00:00",
    "datacenter": {
      "description": "Falkenstein 1 DC 8",
      "id": 1,
      "location": {
        "city": "Falkenstein",
        "country": "DE",
        "description": "Falkenstein DC Park 1",
        "id": 1,
        "latitude": 50.47612,
        "longitude": 12.370071,
        "name": "fsn1",
        "network_zone": "eu-central"
      },
      "name": "fsn1-dc8",
      "server_types": {
        "available": [
          1,
          2,
          3
        ],
        "available_for_migration": [
          1,
          2,
          3
        ],
        "supported": [
          1,
          2,
          3
        ]
      }
    },
    "id": 42,
    "image": {
      "bound_to": null,
      "created": "2016-01-30T23:50:00+00:00",
      "created_from": {
        "id": 1,
        "name": "Server"
      },
      "deleted": null,
      "deprecated": "2018-02-28T00:00:00+00:00",
      "description": "Ubuntu 20.04 Standard 64 bit",
      "disk_size": 10,
      "id": 4711,
      "image_size": 2.3,
      "labels": {
        "env": "dev"
      },
      "name": "ubuntu-20.04",
      "os_flavor": "ubuntu",
      "os_version": "20.04",
      "protection": {
        "delete": false
      },
      "rapid_deploy": false,
      "status": "available",
      "type": "snapshot"
    },
    "included_traffic": 654321,
    "ingoing_traffic": 123456,
    "iso": {
      "deprecated": "2018-02-28T00:00:00+00:00",
      "description": "FreeBSD 11.0 x64",
      "id": 4711,
      "name": "FreeBSD-11.0-RELEASE-amd64-dvd1",
      "type": "public"
    },
    "labels": {
      "env": "dev"
    },
    "load_balancers": [],
    "locked": false,
    "name": "my-server",
    "outgoing_traffic": 123456,
    "primary_disk_size": 50,
    "private_net": [
      {
        "alias_ips": [],
        "ip": "10.0.0.2",
        "mac_address": "86:00:ff:2a:7d:e1",
        "network": 4711
      }
    ],
    "protection": {
      "delete": false,
      "rebuild": false
    },
    "public_net": {
      "firewalls": [
        {
          "id": 38,
          "status": "applied"
        }
      ],
      "floating_ips": [
        478
      ],
      "ipv4": {
        "blocked": false,
        "dns_ptr": "server01.example.com",
        "ip": "1.2.3.4"
      },
      "ipv6": {
        "blocked": false,
        "dns_ptr": [
          {
            "dns_ptr": "server.example.com",
            "ip": "2001:db8::1"
          }
        ],
        "ip": "2001:db8::/64"
      }
    },
    "rescue_enabled": false,
    "server_type": {
      "cores": 1,
      "cpu_type": "shared",
      "deprecated": true,
      "description": "CX11",
      "disk": 25,
      "id": 1,
      "memory": 1,
      "name": "cx11",
      "prices": [
        {
          "location": "fsn1",
          "price_hourly": {
            "gross": "1.1900000000000000",
            "net": "1.0000000000"
          },
          "price_monthly": {
            "gross": "1.1900000000000000",
            "net": "1.0000000000"
          }
        }
      ],
      "storage_type": "local"
    },
    "status": "initializing",
    "volumes": []
  }
}
```



