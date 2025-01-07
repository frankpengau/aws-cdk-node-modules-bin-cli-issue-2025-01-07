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

### Other notes

Following tests are spinning up temporary docker container with ubuntu and installing npm and node:
<details>
<summary>Mini Test Setup...(open to see more)</summary>

```bash
# Install ubuntu and run in temporary container in interactive mode (-it) with self cleanup (--rm) after exit
docker run -it --rm ubuntu
# Install node and npm
apt-get install -y nodejs npm

# npx call aws-cdk and using cdk doctor --verbose
npx aws-cdk doctor --verbose

# Install globally aws-cdk
npm install -g aws-cdk
# npx 2nd call aws-cdk and using cdk doctor --verbose
npx aws-cdk doctor --verbose

# Uninstall globally aws-cdk
npm uninstall -g aws-cdk
# npx 3rd call aws-cdk and using cdk doctor --verbose
npx aws-cdk doctor --verbose
```
</details>

<details>
<summary>`npx aws-cdk doctor --verbose` without installing via `npm install -g aws-cdk` test output...(open to see more)</summary>

```bash
root@2af5db56fcc1:/# npx aws-cdk doctor --verbose
[16:45:36] CDK toolkit version: 2.174.0 (build 9604329)
[16:45:36] Command line arguments: {
  _: [ 'doctor' ],
  verbose: 1,
  v: 1,
  app: undefined,
  a: undefined,
  build: undefined,
  context: [],
  c: [],
  plugin: [],
  p: [],
  trace: undefined,
  strict: undefined,
  lookups: true,
  'ignore-errors': false,
  ignoreErrors: false,
  json: false,
  j: false,
  debug: false,
  profile: undefined,
  proxy: undefined,
  'ca-bundle-path': undefined,
  caBundlePath: undefined,
  ec2creds: undefined,
  i: undefined,
  'version-reporting': undefined,
  versionReporting: undefined,
  'path-metadata': undefined,
  pathMetadata: undefined,
  'asset-metadata': undefined,
  assetMetadata: undefined,
  'role-arn': undefined,
  r: undefined,
  roleArn: undefined,
  staging: true,
  output: undefined,
  o: undefined,
  notices: undefined,
  'no-color': false,
  noColor: false,
  ci: false,
  unstable: [],
  '$0': 'root/.npm/_npx/fa14b75510cd2922/node_modules/.bin/cdk'
}
[16:45:36] merged settings: {
  versionReporting: true,
  assetMetadata: true,
  pathMetadata: true,
  output: 'cdk.out',
  context: {},
  debug: false,
  plugin: [],
  toolkitBucket: {},
  staging: true,
  bundlingStacks: [],
  lookups: true,
  hotswap: { ecs: {} },
  unstable: []
}
[16:45:36] Reading cached notices from /root/.cdk/cache/notices.json
[16:45:36] Looking up AWS region in the EC2 Instance Metadata Service (IMDS).
[16:45:36] Unable to retrieve AWS region from IMDS: Error: Error fetching metadata token: Error: connect ECONNREFUSED 169.254.169.254:80
[16:45:36] Unable to determine AWS region from environment or AWS configuration (profile: "default"), defaulting to 'us-east-1'
[16:45:36] Looking up AWS region in the EC2 Instance Metadata Service (IMDS).
[16:45:36] Unable to retrieve AWS region from IMDS: Error: Error fetching metadata token: Error: connect ECONNREFUSED 169.254.169.254:80
[16:45:36] Unable to determine AWS region from environment or AWS configuration (profile: "default"), defaulting to 'us-east-1'
[16:45:36] Toolkit stack: CDKToolkit
ℹ️ CDK Version: 2.174.0 (build 9604329)
ℹ️ No AWS environment variables
ℹ️ No CDK environment variables
[16:45:36] Reading cached notices from /root/.cdk/cache/notices.json
root@2af5db56fcc1:/#
```
</details>


<details>
<summary>`npx aws-cdk doctor --verbose` after installing `npm install -g aws-cdk` test output...(open to see more)</summary>

```bash
root@2af5db56fcc1:/# npx aws-cdk doctor --verbose
[16:46:59] CDK toolkit version: 2.174.0 (build 9604329)
[16:46:59] Command line arguments: {
  _: [ 'doctor' ],
  verbose: 1,
  v: 1,
  app: undefined,
  a: undefined,
  build: undefined,
  context: [],
  c: [],
  plugin: [],
  p: [],
  trace: undefined,
  strict: undefined,
  lookups: true,
  'ignore-errors': false,
  ignoreErrors: false,
  json: false,
  j: false,
  debug: false,
  profile: undefined,
  proxy: undefined,
  'ca-bundle-path': undefined,
  caBundlePath: undefined,
  ec2creds: undefined,
  i: undefined,
  'version-reporting': undefined,
  versionReporting: undefined,
  'path-metadata': undefined,
  pathMetadata: undefined,
  'asset-metadata': undefined,
  assetMetadata: undefined,
  'role-arn': undefined,
  r: undefined,
  roleArn: undefined,
  staging: true,
  output: undefined,
  o: undefined,
  notices: undefined,
  'no-color': false,
  noColor: false,
  ci: false,
  unstable: [],
  '$0': 'usr/local/bin/cdk'
}
[16:46:59] merged settings: {
  versionReporting: true,
  assetMetadata: true,
  pathMetadata: true,
  output: 'cdk.out',
  context: {},
  debug: false,
  plugin: [],
  toolkitBucket: {},
  staging: true,
  bundlingStacks: [],
  lookups: true,
  hotswap: { ecs: {} },
  unstable: []
}
[16:46:59] Reading cached notices from /root/.cdk/cache/notices.json
[16:46:59] Looking up AWS region in the EC2 Instance Metadata Service (IMDS).
[16:47:00] Unable to retrieve AWS region from IMDS: Error: Error fetching metadata token: TimeoutError: Socket timed out without establishing a connection within 1000 ms
[16:47:00] Unable to determine AWS region from environment or AWS configuration (profile: "default"), defaulting to 'us-east-1'
[16:47:00] Looking up AWS region in the EC2 Instance Metadata Service (IMDS).
[16:47:00] Unable to retrieve AWS region from IMDS: Error: Error fetching metadata token: Error: connect ECONNREFUSED 169.254.169.254:80
[16:47:00] Unable to determine AWS region from environment or AWS configuration (profile: "default"), defaulting to 'us-east-1'
[16:47:00] Toolkit stack: CDKToolkit
ℹ️ CDK Version: 2.174.0 (build 9604329)
ℹ️ No AWS environment variables
ℹ️ No CDK environment variables
[16:47:00] Reading cached notices from /root/.cdk/cache/notices.json
root@2af5db56fcc1:/#
```
</details>