
# PluginDatabase for [Millennium](https://github.com/SteamClientHomebrew/Millennium)

[Home Page](https://steambrew.app/) • [Discord](https://steambrew.app/discord) • [Documentation](https://docs.steambrew.app/)

A centralized repository that manages and curates all community and official plugins for [Millennium](https://github.com/SteamClientHomebrew/Millennium).
This repository exists to provide a secure, version-controlled collection of plugins that are approved for use with Millennium. Each plugin is tracked as a Git submodule, allowing us to:

* Independently version plugins without relying on the latest changes from their original repositories.
* Manually review all plugin updates before they reach end users, ensuring code integrity and preventing malicious behavior.
* Provide a consistent, reliable plugin experience across all installations of Millennium.

Whether you're a plugin developer submitting updates or a user browsing available extensions, this database serves as the trusted source for all Millennium-compatible plugins.

## Submitting A Plugin[^1]

To submit a plugin, open a pull request that adds your repository as a submodule. From the root of this repository, run:

```
git submodule add https://github.com/YourUsername/YourRepository plugins/your-plugin
```

This pins your plugin at a specific commit. Updates to your repository won't appear here until you open a pull request to advance the pointer — this is intentional, as all code changes are audited before reaching users.

## Updating Your Plugin[^2]

To update your plugin to a newer commit, pull from inside the submodule directory, then commit the pointer change in the parent repo:

```
git submodule update --remote plugins/your-plugin
git commit -m "chore: update your-plugin"
```

Then open a pull request with that commit.

To clone all plugins at their pinned commits after a fresh checkout, run `git submodule update --init`.

[^1]: Submitting A Plugin
[^2]: Updating Your Plugin
