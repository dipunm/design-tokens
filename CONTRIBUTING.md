First of all, thank you for contributing. It’s appreciated.

# To submit a pull request

1. Open a GitHub issue before doing significant amount of work and engage with design team.
2. Clone the repo. If it was already cloned, then git pull to get the latest from master.
3. Run `npm install` before anything else, and wait.
4. Write code.
5. Make sure tests pass (`npm run test`) and make a pull request against the master branch. If you are adding a new token, make sure to update the related READMEs ([main radme](https://github.com/opentable/design-tokens/blob/master/README.md) and design-system specific: [ottheme readme](https://github.com/opentable/design-tokens/blob/master/OTTheme/README.md) or [otkit readme](https://github.com/opentable/design-tokens/blob/master/OTKit/README.md) )


# To release new versions

1. To check what needs to be published run `npm run updated`.
2. Make sure you are listed among the collaborators for the related packages that you want to release and that you are logged in with that  account to npm. To check if you are among the allowed collaborators of a specific token: `curl https://www.npmjs.com/package/<token-name>/collaborators` ([example](https://www.npmjs.com/package/otkit-typography/collaborators)). If you aren't just rechout to any of the person listed and ask to be added.
3. To publish run `npm run publish` and follow the instruction on the terminal. The CLI will walk you through the publishing for each token that need to published.

## Version cheat sheet:
- **Patch version (0.0.x)** -> Release a patch when you make backwards-compatible bug fixes. This means that for a specific design-system some values are corrected and updated (ie: a color get updated)
- **Minor version (0.x.0)** -> Release a minor when you add functionality in a backwards-compatible manner. This means that for a specific design-system you are adding new decisions (ie: a new color is added)
- **Major version (x.0.0)** -> Release a major when you make incompatible changes. This means that for a specific design system some values where removed (ie: a color was removed)
