# gitbook-cli

[![NPM version](https://badge.fury.io/js/gitbook-cli.svg)](http://badge.fury.io/js/gitbook-cli)
[![Linux Build Status](https://travis-ci.org/GitbookIO/gitbook-cli.png?branch=master)](https://travis-ci.org/GitbookIO/gitbook-cli)
[![Windows Build status](https://ci.appveyor.com/api/projects/status/gddbj0602joc4wah?svg=true)](https://ci.appveyor.com/project/GitBook/gitbook-cli)

> The GitBook command line interface.

Install this globally and you'll have access to the gitbook command anywhere on your system.

```
$ npm install -g gitbook-cli
```

**Note:** The purpose of the gitbook command is to load and run the version of GitBook you have specified in your book (or the latest one), irrespective of its version. The GitBook CLI only support versions `>=2.0.0` of GitBook.

`gitbook-cli` store GitBook's versions into `~/.gitbook`, you can set the `GITBOOK_DIR` environment variable to use another directory.

## How to install it?

```
$ npm install -g gitbook-cli
```

## How to use it?

#### Build and Serve

Build a book in the curent directory using:

```
$ gitbook build
```

Build a book in another directory:

```
$ gitbook build ./other_folder
```

Build and serve the book:

```
$ gitbook serve ./
```

List all available commands using:
```
$ gitbook help
```

#### Specify a specific version

By default, GitBook CLI will read the gitbook version to use from the book configuration, but you can force a specific version using `--gitbook` option:

```
$ gitbook build ./mybook --gitbook=2.0.1
```

and list available commands in this version using:

```
$ gitbook help --gitbook=2.0.1
```

#### Manage versions

List installed versions:

```
$ gitbook versions
```

List available versions:

```
$ gitbook versions:available
```

Install a specific version:

```
$ gitbook versions:install 2.1.0

# or a pre-release

$ gitbook versions:install beta
```

Update to the latest version

```
$ gitbook versions:update
```

Uninstall a specific version

```
$ gitbook versions:uninstall 2.0.1
```

Use a local folder as a GitBook version (for developement)

```
$ gitbook versions:link ./mygitbook
```
