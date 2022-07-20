**⚠ Only [Core CMS] and [Core Styles] are supported and tested. ⚠️**

# TACC Core Workspace

Workspace for simultaneous development of TACC WMA Workspace Portals & Websites

## Related Repositories

- [Core CMS], the base CMS code for TACC WMA CMS Websites
- [Core Portal], the base Portal code for TACC WMA CMS Websites
- [Core Styles], the shared UI pattern code for TACC WMA CMS Websites
- [Core Components], the shared JS components for TACC WMA CMS Websites

## Local Development Setup

1. Install package dependencies, from root, via `npm ci`.
2. Clone/Move [Core CMS] and [tup-ui (for Core Styles)][Core Styles] into this root directory.
    - After cloning, follow each package's README instructions.
    - Moving an existing repository works just as well.

### Known Issues

1. After `npm ci`, the `postinstall` script results in the error "✖ Failed to symlink [...]core-styles with error: [...]"—it does __not__ affect development (because the [Core Styles] CLI is not used by clients; it may even be removed.) For more information see [privatenumber/link#10][cli-symlink-error].

## Using the Packages

Each package:

- shares dependencies (which have been hoisted to root)
- can load each other as if the other is an NPM package

You may:

- Perform any desired development within a package.
- Run, from root, a convenience script e.g.:
  - `npm run core-cms:demo --project=core-cms`
  - `npm run core-cms:demo --project=frontera-cms`
  - `npm run core-styles:demo`
- Run, from root, a script of any package e.g.:
  - `npm run core-cms: npm run build:css`
  - `npm run core-cms: npm run build:demo`
  - `npm run core-styles: npm run build`
  - `npm run core-styles: npm run start`

### Known Issues

1. If `npm install (...)` is run _in a package_, then core-styles package is unlinked (which can cause build errors). To restore the link, run `npm ci` _in root_.

<!-- Link Aliases -->

[Core CMS]: https://github.com/TACC/Core-CMS
[Core Styles]: https://github.com/TACC/tup-ui/tree/main/libs/core-styles
[Core Components]: https://github.com/TACC/tup-ui/tree/main/libs/core-components
[Core Portal]: https://github.com/TACC/Core-Portal

[cli-symlink-error]: https://github.com/privatenumber/link/issues/10
