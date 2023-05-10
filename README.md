# Instructions

## Development

### Linking Local NPM Project

- See more info [here](https://medium.com/dailyjs/how-to-use-npm-link-7375b6219557).
- Linking:
  - Navigate to local directory of npm dependency, for example `some-dep`.
  - Execute `npm link` to create a global link.
  - Navigate to the project that will use the npm dependency.
  - Execute `npm link @scope/some-dep` to create a local link. Use full package name, including scope.
- Unlinking:
  - Navigate to the project that will use the npm dependency.
  - Execute `npm uninstall --no-save @scope/some-dep && npm install ` to remove the local link.
  - Navigate to local directory of npm dependency, for example `some-dep`.
  - Execute `npm unlink` to remove the global link.
