# Open Standard Documentation

Smart Resource Connect advocates for an open standard for describing surplus resources and demands, facilitating global interoperability.

## Surplus Resource Schema

```json
{
  "id": "string",
  "title": "string",
  "description": "string",
  "category": "string",
  "quantity": "number",
  "unit": "string",
  "location": "string",
  "availableUntil": "string",
  "provider": "string",
  "status": "string",
  "postedAt": "string"
}
```

## Demand Schema

```json
{
  "id": "string",
  "title": "string",
  "description": "string",
  "category": "string",
  "quantity": "number",
  "unit": "string",
  "location": "string",
  "neededBy": "string",
  "requester": "string",
  "status": "string",
  "postedAt": "string"
}
``` 