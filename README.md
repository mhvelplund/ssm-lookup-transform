# SSM variable lookup transform

A Cloudformation macro for looking up dynamic SSM keys.

Example:

```yaml
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  Project:
    Type: String
Resources:
  ArtifactBucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      BucketName:
        'Fn::Transform':
          - Name: SsmLookup
            Parameters:
              Key: !Sub '/projects/${Project}'
```