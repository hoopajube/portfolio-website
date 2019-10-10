# portfolio-website


# aws cli cloudformation pipeline deployment
```
aws cloudformation create-stack --capabilities CAPABILITY_IAM --parameters ParameterKey=BuildComputeType,ParameterValue=BUILD_GENERAL1_SMALL,ParameterKey=BuildImage,ParameterValue=aws/codebuild/ubuntu-base=14.04,ParameterKey=BuildType,ParameterValue=LINUX_CONTAINER,ParameterKey=GitHubBranch,ParameterValue=master,ParameterKey=GitHubRepo,ParameterValue=portfolio-website,ParameterKey=GitHubToken,ParameterValue=,ParameterKey=GitHubUser,ParameterValue=alexpereyra,ParameterKey=SiteBucketName,ParameterValue=alexander.pereyra.info --stack-name portfolio-website --template-body file://pipeline.json --region us-east-1
```
```
aws cloudformation --validate-template --template-body file://pipeline.json
```
