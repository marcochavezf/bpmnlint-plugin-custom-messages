# bpmnlint-plugin-custom

[![Build Status](https://travis-ci.org/bpmn-io/bpmnlint-plugin-custom.svg?branch=master)](https://travis-ci.org/bpmn-io/bpmnlint-plugin-custom)

An custom [bpmnlint](https://github.com/bpmn-io/bpmnlint) plug-in.


## About

This plugin shows how to contribute [rules](#add-rules) and
[configuration](#add-configuration) to bpmnlint.


## Add Rules

The [`./rules`](./rules) folder contains rules that are made available via
this plug-in. Configure them with the `custom` prefix in your `.bpmnlintrc`:

```json
{
  "rules": {
    "custom/no-manual-task": "warn"
  }
}
```

Checkout [`./test.js`](./test.js) to learn how to test your rules.


## Add Configuration

As part of the [`./index.js`](./index.js) the plug-in exposes configurations
to extend from using `extends` in the bpmnlint configuration:

```json
{
  "extends": [
    "bpmnlint:recommended",
    "plugin:custom/recommended"
  ]
}
```


## License

MIT
