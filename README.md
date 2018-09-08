# SSM variable lookup transform

Cloudformation helpers for looking up dynamic SSM keys.

* `SsmLookup.yml`: Defines a transform function that returns the latest version of an SSM key.
* `SsmReplace.yml`: Defines a transform macro that can be used to replace keys in an entire
  template.

The `examples` folder contains demonstration CloudFormation stacks.

Both helpers support providing a default value that is used if the SSM key doesn't exist.