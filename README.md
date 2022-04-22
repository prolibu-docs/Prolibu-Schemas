# Prolibu-Schemas
Schema field reference
```json
{
  text: {
    type: 'string'
  },
  datetime: {
    type: 'datetime'
  },
  currency: {
    model: 'currency'
  },
  number: {
    type: 'float', // OR Number
    defaultsTo: 0,
    skipAll: true
  },
  list: {
    type: 'string',
    defaultsTo: 'Draft',
    enum: [
      'Draft',
      'Ready',
      'Approved',
      'Denied'
    ]
  },
  searhModel: {
    required: true,
    description: 'User who created the resource',
    model: 'model',
    skipAll: true
  },
}
```
