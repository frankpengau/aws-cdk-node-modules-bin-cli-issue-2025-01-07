# Welcome to your CDK TypeScript project

This is a blank project for CDK development with TypeScript.

The `cdk.json` file tells the CDK Toolkit how to execute your app.

## Useful commands

* `npm run build`   compile typescript to js
* `npm run watch`   watch for changes and compile
* `npm run test`    perform the jest unit tests
* `npx cdk deploy`  deploy this stack to your default AWS account/region
* `npx cdk diff`    compare deployed stack with current state
* `npx cdk synth`   emits the synthesized CloudFormation template

## Check cli
Ensure using aws cli to match aws-cdk-lib

```
node ./node_modules/aws-cdk/bin/cdk.js
npx ts-node ./node_modules/aws-cdk/bin/cdk.js

./node_modules/aws-cdk/bin/cdk
./node_modules/.bin/cdk

npx which cdk
npx aws-cdk doctor
npx aws-cdk doctor --verbose
```