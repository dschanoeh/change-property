# Change Property

![Tests](https://github.com/dschanoeh/change-property/actions/workflows/test.yaml/badge.svg)

This is a GitHub Action to change a single property in a [Java .properties files](https://en.wikipedia.org/wiki/.properties).


## Inputs

### `file` (required)
The path of the properties file to be modified.

### `property` (required)
The property key to be modified. If the property doesn't exist,
a new entry will be added to the file. Otherwise, it will be
replaced in-line.

### `value` (required)
The value to be written.

### `create` (optional)
When set to `'true'`, the file will be created if it doesn't exist.

## Usage

```
- name: Change property
  uses: dschanoeh/change-property@1.0.0
  with:
    file: my.properties
    property: foo
    value: val
```
