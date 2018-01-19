# Microsoft.Cache/Redis template reference
API Version: 2017-10-01
## Template format

To create a Microsoft.Cache/Redis resource, add the following JSON to the resources section of your template.

```json
{
  "name": "string",
  "type": "Microsoft.Cache/Redis",
  "apiVersion": "2017-10-01",
  "properties": {
    "redisConfiguration": {},
    "enableNonSslPort": boolean,
    "tenantSettings": {},
    "shardCount": "integer",
    "sku": {
      "name": "string",
      "family": "string",
      "capacity": "integer"
    },
    "subnetId": "string",
    "staticIP": "string"
  },
  "zones": [
    "string"
  ],
  "location": "string",
  "tags": {},
  "resources": []
}
```
## Property values

The following tables describe the values you need to set in the schema.

<a id="Microsoft.Cache/Redis" />
### Microsoft.Cache/Redis object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  name | string | Yes |  |
|  type | enum | Yes | Microsoft.Cache/Redis |
|  apiVersion | enum | Yes | 2017-10-01 |
|  properties | object | Yes | Redis cache properties. - [RedisCreateProperties object](#RedisCreateProperties) |
|  zones | array | No | A list of availability zones denoting where the resource needs to come from. - string |
|  location | string | Yes | The geo-location where the resource lives |
|  tags | object | No | Resource tags. |
|  resources | array | No | [linkedServers](./Redis/linkedServers.md) [firewallRules](./Redis/firewallRules.md) |


<a id="RedisCreateProperties" />
### RedisCreateProperties object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  redisConfiguration | object | No | All Redis Settings. Few possible keys: rdb-backup-enabled,rdb-storage-connection-string,rdb-backup-frequency,maxmemory-delta,maxmemory-policy,notify-keyspace-events,maxmemory-samples,slowlog-log-slower-than,slowlog-max-len,list-max-ziplist-entries,list-max-ziplist-value,hash-max-ziplist-entries,hash-max-ziplist-value,set-max-intset-entries,zset-max-ziplist-entries,zset-max-ziplist-value etc. |
|  enableNonSslPort | boolean | No | Specifies whether the non-ssl Redis server port (6379) is enabled. |
|  tenantSettings | object | No | A dictionary of tenant settings |
|  shardCount | integer | No | The number of shards to be created on a Premium Cluster Cache. |
|  sku | object | Yes | The SKU of the Redis cache to deploy. - [Sku object](#Sku) |
|  subnetId | string | No | The full resource ID of a subnet in a virtual network to deploy the Redis cache in. Example format: /subscriptions/{subid}/resourceGroups/{resourceGroupName}/Microsoft.{Network|ClassicNetwork}/VirtualNetworks/vnet1/subnets/subnet1 |
|  staticIP | string | No | Static IP address. Required when deploying a Redis cache inside an existing Azure Virtual Network. |


<a id="Sku" />
### Sku object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  name | enum | Yes | The type of Redis cache to deploy. Valid values: (Basic, Standard, Premium). - Basic, Standard, Premium |
|  family | enum | Yes | The SKU family to use. Valid values: (C, P). (C = Basic/Standard, P = Premium). - C or P |
|  capacity | integer | Yes | The size of the Redis cache to deploy. Valid values: for C (Basic/Standard) family (0, 1, 2, 3, 4, 5, 6), for P (Premium) family (1, 2, 3, 4). |
