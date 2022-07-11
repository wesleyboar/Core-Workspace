**⚠ Only [Core CMS] and [Core Styles] are supported and tested. ⚠️**

# TACC Core Workspace

Workspace for simultaneous development of TACC WMA Workspace Portals & Websites

## Related Repositories

- [Core CMS], the base CMS code for TACC WMA CMS Websites
- [Core Portal], the base Portal code for TACC WMA CMS Websites
- [Core Styles], the shared UI pattern code for TACC WMA CMS Websites
- [Core Components], the shared JS components for TACC WMA CMS Websites

## Local Development Setup

1. Install dependencies: `npm ci`.
    - You may ignore an error about symlinking `core-styles/src/cli.js`.[^1]
2. Clone/Copy [Core CMS] and [Core Styles] into this root directory.
    - If cloning, follow each project's README instructions.
3. (Optional) Perform any desired development within a project.
4. Run any project script from root e.g.:
    - `npm run core-cms: npm run build`
    - `npm run core-cms: npm run start`
    - `npm run core-styles: npm run build`
    - `npm run core-styles: npm run start`

[^1]: The error "✖ Failed to symlink [...]core-styles with error: [...]" is concerning, but does not affect development. (The [Core Styles] CLI is not used by clients, and might be removed.)

<!-- Link Aliases -->

[Core CMS]: https://github.com/TACC/Core-CMS
[Core Styles]: https://github.com/TACC/tup-ui/tree/main/libs/core-styles
[Core Components]: https://github.com/TACC/tup-ui/tree/main/libs/core-components
[Core Portal]: https://github.com/TACC/Core-Portal
