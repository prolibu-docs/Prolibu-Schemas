# Prolibu-Schemas
Schema field reference

## Field Names
In camel case style 
Example:
- vitrinaDeCierre
- facturaNombreLead

## Fields Attributes
- type (string, datetime, longtext, number, float, boolean)
- enum
- model 
- defaultsTo
- required
- description

## Special Types 
- Enum: lists

## Example
```json
{
  "text": {
    "type": "string"
  },
  "datetime": {
    "type": "datetime"
  },
  "currency": {
    "model": "currency"
  },
  "number": {
    "type": "float",
    "defaultsTo": 0
  },
  "list": {
    "type": "string",
    "defaultsTo": "Draft",
    "enum": [
      "Draft",
      "Ready",
      "Approved",
      "Denied"
    ]
  },
  "searhModel": {
    "required": true,
    "description": "User who created the resource",
    "model": "model"
  },
  "alsoNotifyViewsTo": {
    "description": "Also notify these users when someone is watching the proposal",
    "type": "array",
    "multiple": "user"
  }
}
```

© 2021 PROLIBU TECH SAS, ALL RIGHTS RESERVED.
