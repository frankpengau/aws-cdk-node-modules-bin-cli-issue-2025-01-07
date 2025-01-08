# aws-cdk-node-modules-bin-cli-issue-2025-01-07

Issues in question from following PRs:
- https://github.com/aws/aws-cdk/pull/32476
- https://github.com/aws/aws-cdk/pull/32518
- https://github.com/aws/aws-cdk/pull/32514

```bash
./node_modules/aws-cdk/bin/cdk.js

./node_modules/aws-cdk/bin/cdk
./node_modules/.bin/cdk

npx which cdk

npx aws-cdk --version
npx aws-cdk doctor
npx aws-cdk doctor --verbose
```

v2.173.1
- In `node_modules/aws-cdk/bin`:
  - `cdk`
  - `cdk.js`
  - `cdk.d.ts`

v2.174.0
- In `node_modules/aws-cdk/bin`:
  - `cdk`

