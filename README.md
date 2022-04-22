# Prolibu-Schemas
Schema field reference

## Fields Attributes
---
- model 
- type (string, datetime, longtext)
- required
- description

## Example
---
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
    "type": "float", // OR Number
    "defaultsTo": 0,
    "skipAll": true
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
    "model": 'model',
    "skipAll": true
  },
  "alsoNotifyViewsTo": {
    "description": "Also notify these users when someone is watching the proposal",
    "type": "array",
    "multiple": "user"
  }
}
```

© 2021 PROLIBU TECH SAS, ALL RIGHTS RESERVED.
