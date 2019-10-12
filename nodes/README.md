# Test data of nodes
This test data format is [YAML](https://github.com/yaml/yaml).

## Test Data
```yaml
- name: "" # test name
  jfol: ""
  nodes:
    - text: "" # some nodes
```

## Node
### Text
```yaml
text: ""
```

### Literal
string:
```yaml
stringValue: ""
```

boolean:
```yaml
booleanValue: true
```

number:
```yaml
numberValue: 0
```

null:
```yaml
nullValue: null
```

### Operator
```yaml
operator: "==" # Operator Type
```

#### Operator Type
```ts
export type Operator = "==" | "!=" | "+" | "-" | "%" | "*" | "/" | "&&" | "||" | "<" | "<=" | ">" | ">=";
```

### Field
```yaml
fieldNodes:
  - fieldIdentifier: ""
fieldBodies: # optional
  - text: "" # some nodes
```

### Function
```yaml
functionNodes:
  - functionIdentifier: ""
functionArguments: # optional
  - booleanValue: true # some expression
functionBodies: # optional
  - text: "" # some nodes
```

### Expression
```yaml
expression:
  - booleanValue: true # some Field or Function or Literal or Operator or Expression
```