# KNOWN ISSUES

1. AmazonCloudWatchEventRule Id can't be greater than 64 characters.  Design a better name.

Use something like 
```
 BucketWithSemiRandomName:
    Type: AWS::S3::Bucket
    Properties:
      BucketName:
        !Sub
          - 'bucket-with-semi-random-name-${RandomGUID}'
          - { RandomGUID: !Select [0, !Split ["-", !Select [2, !Split ["/", !Ref AWS::StackId ]]]] }
```