# ts-clean-built

> Safely removes built `*.js  *.d.ts *.js.map` files from directory excluding.

## Install

![npm (scoped)](https://img.shields.io/npm/v/ts-clean-built.svg?maxAge=86400) [![Build Status](https://travis-ci.org/whitecolor/ts-clean-built.svg?branch=master)](https://travis-ci.org/whitecolor/ts-clean-built)

```
yarn add clean-ts-built --dev
```

## Usage

```
ts-clean-built [--old|--all] [--exclude folder1 folder2] [dir]
```

- By default (without flags) searches `.ts` files and removes corresponding `.js, .d.ts, .js.map`.

- `--old` - will search `.d.ts` files and remove corresponding `.js, .js.map` if no `.ts/tsx` version exists.

- `--allow-dts` - used with `--old`, will not remove `.d.ts` if no corresponding `.ts` or `.js` exists, allowing to have leave `.d.ts` files.

- `--all` - will remove all found `.js, .d.ts, .js.map` files, **potentially dangerous** option.

- `--dot` - dot-folders excluded use  flag or `ts-built .my-dot-folder`.

- `--quite` - will not output log messages.

- `--exclude` - list of patterns to exclude from search, i.e. `--exclude **/my-folder/**` will exclude all files in all directories named `my-folder` in the tree.

  `node_modules`, `bower_components`, `jspm_packages` are excluded by default.

- `--dry` - will not remove files, just show the list to going to delete.

- `--files` - outputs list of files removed.

- `dir` - is '.' (cwd) by default


## Licence

MIT.
