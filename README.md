# Prolibu-Schemas
Schema field reference

## Field Names
Camel case style. Example:
- vitrinaDeCierre
- facturaNombreLead

## Field Attributes
- type (string, datetime, longtext, number, float, boolean)
- enum
- model 
- defaultsTo
- required
- description
- url

## Special Types 
- Enum: lists

## Considerations
- url attribute: make remote search to custom or external endpoint
- formSchema: allow add form in json field

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
  "balanceados": {
    "type": "json",
    "label": "Activos Balanceados",
    "formSchema": {
      "BConservador": {
        "type": "float",
         "label": "B.Conservador"
      },
      "BModerado": {
        "type": "float",
         "label": "B.Moderado"
      },
      "BCrecimiento": {
        "type": "float",
         "label": "B.Crecimiento"
      }
    }
  },
  "marca": {
    "type": "string",
    "scope": "abc0",
    "label": "Buscar Marca",
    "url": "https://biotronitech-dev.prolibu.com/v1/CustomObjectBiotronitech/searchProduct"
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
