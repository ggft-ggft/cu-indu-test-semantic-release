# semantic-release-npm

[![Semantic Release Badge](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)
[![GitLab Pipeline Status](https://gitlab.com/gitlab-examples/semantic-release-npm/badges/master/pipeline.svg)](https://gitlab.com/gitlab-examples/semantic-release-npm/-/pipelines/latest)

An example project that uses [semantic-release](https://github.com/semantic-release/semantic-release) to automate the publishing of NPM packages to [GitLab's Package Registry](https://docs.gitlab.com/ee/user/packages/npm_registry/index.html).

See the auto-generated releases on the [**Releases** page](https://gitlab.com/gitlab-examples/semantic-release-npm/-/releases) and the auto-published NPM packages on the [**Packages** page](https://gitlab.com/gitlab-examples/semantic-release-npm/-/packages).

A step-by-step guide can be found in [GitLab's CI/CD examples documentation](https://docs.gitlab.com/ee/ci/examples/semantic-release.html).

## Environment variables

As part of publishing a package, semantic-release bumps the version in `package.json`. To allow it to commit this change and push it back to GitLab, the pipeline requires a custom environment variable named `GITLAB_TOKEN`, a project access token with `api` scope. This token can be generated by navigating to **Project > Settings > Access Tokens**. Be sure to mask this variable (otherwise it may be printed in plaintext in the job output).

## Consuming the example module

To use this example module in another project, add the following to the project's `.npmrc`:

```
@gitlab-examples:registry=https://gitlab.com/api/v4/packages/npm/
```

Or, if using Yarn, add this to the project's `.yarnrc`

```
"@gitlab-examples:registry" "https://gitlab.com/api/v4/packages/npm/"
```

Then, install the package:

```bash
npm install --save @gitlab-examples/semantic-release-npm
```

or:

```bash
yarn add @gitlab-examples/semantic-release-npm
```
--blabllbal
--blabllbal