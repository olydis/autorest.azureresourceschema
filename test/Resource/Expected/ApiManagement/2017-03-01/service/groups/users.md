# Microsoft.ApiManagement/service/groups/users template reference
API Version: 2017-03-01
## Template format

To create a Microsoft.ApiManagement/service/groups/users resource, add the following JSON to the resources section of your template.

```json
{
  "name": "string",
  "type": "Microsoft.ApiManagement/service/groups/users",
  "apiVersion": "2017-03-01"
}
```
## Property values

The following tables describe the values you need to set in the schema.

<a id="Microsoft.ApiManagement/service/groups/users" />
### Microsoft.ApiManagement/service/groups/users object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  name | string | Yes | User identifier. Must be unique in the current API Management service instance. |
|  type | enum | Yes | Microsoft.ApiManagement/service/groups/users |
|  apiVersion | enum | Yes | 2017-03-01 |

