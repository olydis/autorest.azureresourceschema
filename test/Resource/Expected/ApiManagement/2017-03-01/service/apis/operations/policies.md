# Microsoft.ApiManagement/service/apis/operations/policies template reference
API Version: 2017-03-01
## Template format

To create a Microsoft.ApiManagement/service/apis/operations/policies resource, add the following JSON to the resources section of your template.

```json
{
  "name": "policy",
  "type": "Microsoft.ApiManagement/service/apis/operations/policies",
  "apiVersion": "2017-03-01",
  "properties": {
    "policyContent": "string"
  }
}
```
## Property values

The following tables describe the values you need to set in the schema.

<a id="Microsoft.ApiManagement/service/apis/operations/policies" />
### Microsoft.ApiManagement/service/apis/operations/policies object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  name | enum | Yes | The identifier of the Policy. - policy |
|  type | enum | Yes | Microsoft.ApiManagement/service/apis/operations/policies |
|  apiVersion | enum | Yes | 2017-03-01 |
|  properties | object | Yes | Properties of the Policy. - [PolicyContractProperties object](#PolicyContractProperties) |


<a id="PolicyContractProperties" />
### PolicyContractProperties object
|  Name | Type | Required | Value |
|  ---- | ---- | ---- | ---- |
|  policyContent | string | Yes | Json escaped Xml Encoded contents of the Policy. |

