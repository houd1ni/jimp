# Releasing Jimp

Make sure to have a `GITHUB_AUTH` token set. And are logged into NPM.

```sh
export GITHUB_AUTH=YOUR_PERSONAL_ACCESS_TOKEN
```

Determine the new version by looking at PR labels and using semantic versioning.

| label       | version | bump  |
| ----------- | ------- | ----- |
| bug         | patch   | 0.0.1 |
| enhancement | minor   | 0.1.0 |
| breaking    | major   | 1.0.0 |

First make sure you're on master and run the following command to bump all package versions and generate a changelog.

```sh
yarn publish:packages [patch || minor || major]
```

Make a github release through the ui and copy over changelog from `CHANGELOG.md`.
