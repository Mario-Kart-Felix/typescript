# typescript
Skip to content
Mario-Kart-Felix
/
typescript
Template
generated from Mario-Kart-Felix/typescript-action
 View license
 0 stars  0 forks
Code
Issues
4
Pull requests
Actions
Projects
1
Wiki
Security
Insights
Settings
Latest commit
@Mario-Kart-Felix
Mario-Kart-Felix
…
42 minutes ago
Git stats
Files
README.md
typescript-action status

Create a JavaScript Action using TypeScript
Use this template to bootstrap the creation of a TypeScript action.🚀

This template includes compilation support, tests, a validation workflow, publishing, and versioning guidance.

If you are new, there's also a simpler introduction. See the Hello World JavaScript Action

Create an action from this template
Click the Use this Template and provide the new repo details for your action

Code in Main
Install the dependencies

$ npm install
Build the typescript and package it for distribution

$ npm run build && npm run package
Run the tests ✔️

$ npm test

 PASS  ./index.test.js
  ✓ throws invalid number (3ms)
  ✓ wait 500 ms (504ms)
  ✓ test runs (95ms)

...
Change action.yml
The action.yml contains defines the inputs and output for your action.

Update the action.yml with your name, description, inputs and outputs for your action.

See the documentation

Change the Code
Most toolkit and CI/CD operations involve async operations so the action is run in an async function.

import * as core from '@actions/core';
...

async function run() {
  try { 
      ...
  } 
  catch (error) {
    core.setFailed(error.message);
  }
}

run()
See the toolkit documentation for the various packages.

Publish to a distribution branch
Actions are run from GitHub repos so we will checkin the packed dist folder.

Then run ncc and push the results:

$ npm run package
$ git add dist
$ git commit -a -m "prod dependencies"
$ git push origin releases/v1
```Replaces every occurrence of the first argument in a string with the second argument.

Input


{{ "Take my protein pills and put my helmet on" | replace: "my", "your" }}

Output

Take your protein pills and put your helmet on

Note: We recommend using the `--license` option for ncc, which will create a license file for all of the production node modules used in your project.

Your action is now published! :rocket: 

See the [versioning documentation](https://github.com/actions/toolkit/blob/master/docs/action-versioning.md)

## Validate

You can now validate the action by referencing `./` in a workflow in your repo (see [test.yml](.github/workflows/test.yml))

```yaml
uses: ./
with:
  milliseconds: 1000
See the actions tab for runs of this action! 🚀

Usage:
After testing you can create a v1 tag to reference the stable and latest V1 action

Releases
No releases published
Create a new release
Packages
No packages published
Publish your first package
Contributors 2
@Mario-Kart-Felix
Mario-Kart-Felix
@dependabot
dependabot[bot]
Languages
Python
76.5%
 
TypeScript
15.8%
 
Roff
5.4%
 
JavaScript
2.3%
© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
