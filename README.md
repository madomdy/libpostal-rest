# Libpostal REST

## API Example


### Parser
`curl -X POST -d '{"query": "100 main st buffalo ny"}' 192.168.99.100:8080/parser`

** Response **
```
[
  {
    "label": "house_number",
    "value": "100"
  },
  {
    "label": "road",
    "value": "main st"
  },
  {
    "label": "city",
    "value": "buffalo"
  },
  {
    "label": "state",
    "value": "ny"
  }
]
```

### Expand
`curl -X POST -d '{"query": "100 main st buffalo ny"}' 192.168.99.100:8080/expand`

** Response **
```
[
  "100 main saint buffalo new york",
  "100 main saint buffalo ny",
  "100 main street buffalo new york",
  "100 main street buffalo ny"
]
```
