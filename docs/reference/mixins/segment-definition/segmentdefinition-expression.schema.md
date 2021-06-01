
# Segment Expression Details  Schema

```
https://ns.adobe.com/xdm/context/segmentdefinition-expression
```

Segment expression data such as expression type, mime type, and expression value.

| [Abstract](../../../abstract.md) | [Extensible](../../../extensions.md) | [Status](../../../status.md) | [Identifiable](../../../id.md) | [Custom Properties](../../../extensions.md) | [Additional Properties](../../../extensions.md) | Defined In |
|----------------------------------|--------------------------------------|------------------------------|--------------------------------|---------------------------------------------|-------------------------------------------------|------------|
| Can be instantiated | Yes | Stable | No | Forbidden | Permitted | [mixins/segment-definition/segmentdefinition-expression.schema.json](mixins/segment-definition/segmentdefinition-expression.schema.json) |
## Schema Hierarchy

* Segment Expression Details  `https://ns.adobe.com/xdm/context/segmentdefinition-expression`
  * [Extensibility base schema](../../datatypes/extensible.schema.md) `https://ns.adobe.com/xdm/common/extensible`


## Segment Expression Details  Example
```json
{
  "xdm:segmentExpression": {
    "xdm:expressionType": "PQL",
    "xdm:mimeType": "pql/text",
    "xdm:value": "personalEmail.address.endsWith(\"testxdmmail.com\", false)"
  }
}
```

# Segment Expression Details  Properties

| Property | Type | Required | Defined by |
|----------|------|----------|------------|
| [xdm:segmentExpression](#xdmsegmentexpression) | `object` | Optional | Segment Expression Details  (this schema) |
| `*` | any | Additional | this schema *allows* additional properties |

## xdm:segmentExpression
### Segment expression

`xdm:segmentExpression`
* is optional
* type: `object`
* defined in this schema

### xdm:segmentExpression Type


`object` with following properties:


| Property | Type | Required |
|----------|------|----------|
| `xdm:expressionType`| string | Optional |
| `xdm:mimeType`| string | Optional |
| `xdm:value`| string | Optional |



#### xdm:expressionType
##### Type

Type of expression, for example, PQL, Query Service, or Adobe Audience Manager.

`xdm:expressionType`
* is optional
* type: `string`

##### xdm:expressionType Type


`string`



##### xdm:expressionType Known Values
| Value | Description |
|-------|-------------|
| `0` | PQL |
| `1` | AAM |
| `2` | QUERYSERVICE |






#### xdm:mimeType
##### Expression mime type

Mime type of the expression. For example, pql/text or application/sql.

`xdm:mimeType`
* is optional
* type: `string`

##### xdm:mimeType Type


`string`


All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5Cw%2B%2F%5B-.%5Cw%5D%2B(%3F%3A%5C%2B%5B-.%5Cw%5D%2B)%3F)):
```regex
\w+/[-.\w]+(?:\+[-.\w]+)?
```








#### xdm:value
##### Value

Actual expression string. The syntax of expression will depend upon specified mime type.

`xdm:value`
* is optional
* type: `string`

##### xdm:value Type


`string`










