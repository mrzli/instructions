# Instructions

## Development

### Setting Up Computer for Developement

- Set up git.

```bash
git config --global user.name "Goran Mržljak"
git config --global user.email "goran.mrzljak@gmail.com"
git config --global core.autocrlf input # convert CRLF to LF on commit, but not vice versa
```

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
  - Execute (from any directory) `npm unlink @scope/some-dep` to remove the global link.
