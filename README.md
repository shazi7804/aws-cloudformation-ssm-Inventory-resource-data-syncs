# AWS System Manager Enable Resource Data Syncs

The CloudFormation Stack of enable System Manager Resource Data Syncs, you can launch CloudFormation StackSet deploy multiple accounts or regions.

## How to use

1. Modify `BucketName`, `BucketRegion` parameters of template `EnableAWSSsmResourceDataSyncs.yaml`.

```yaml
Resources:
      BucketName: "<your-bucket-name>"
      BucketRegion: "<your-bucket-region>"
```

## Deploy

```shell
aws cloudformation create-stack-set --stack-set-name EnableAWSSsmResourceDataSyncs --template-body file://EnableAWSSsmResourceDataSyncs.yaml --permission-model SERVICE_MANAGED --auto-deployment Enabled=true,RetainStacksOnAccountRemoval=true
```



