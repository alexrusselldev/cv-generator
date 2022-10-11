oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g cv-generator
$ cv-generator COMMAND
running command...
$ cv-generator (--version)
cv-generator/0.0.0 darwin-x64 node-v16.15.0
$ cv-generator --help [COMMAND]
USAGE
  $ cv-generator COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`cv-generator hello PERSON`](#cv-generator-hello-person)
* [`cv-generator hello world`](#cv-generator-hello-world)
* [`cv-generator help [COMMAND]`](#cv-generator-help-command)
* [`cv-generator plugins`](#cv-generator-plugins)
* [`cv-generator plugins:install PLUGIN...`](#cv-generator-pluginsinstall-plugin)
* [`cv-generator plugins:inspect PLUGIN...`](#cv-generator-pluginsinspect-plugin)
* [`cv-generator plugins:install PLUGIN...`](#cv-generator-pluginsinstall-plugin-1)
* [`cv-generator plugins:link PLUGIN`](#cv-generator-pluginslink-plugin)
* [`cv-generator plugins:uninstall PLUGIN...`](#cv-generator-pluginsuninstall-plugin)
* [`cv-generator plugins:uninstall PLUGIN...`](#cv-generator-pluginsuninstall-plugin-1)
* [`cv-generator plugins:uninstall PLUGIN...`](#cv-generator-pluginsuninstall-plugin-2)
* [`cv-generator plugins update`](#cv-generator-plugins-update)

## `cv-generator hello PERSON`

Say hello

```
USAGE
  $ cv-generator hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/alexrusselldev/cv-generator/blob/v0.0.0/dist/commands/hello/index.ts)_

## `cv-generator hello world`

Say hello world

```
USAGE
  $ cv-generator hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ cv-generator hello world
  hello world! (./src/commands/hello/world.ts)
```

## `cv-generator help [COMMAND]`

Display help for cv-generator.

```
USAGE
  $ cv-generator help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for cv-generator.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.14/src/commands/help.ts)_

## `cv-generator plugins`

List installed plugins.

```
USAGE
  $ cv-generator plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ cv-generator plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.1.1/src/commands/plugins/index.ts)_

## `cv-generator plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ cv-generator plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.

  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.

ALIASES
  $ cv-generator plugins add

EXAMPLES
  $ cv-generator plugins:install myplugin 

  $ cv-generator plugins:install https://github.com/someuser/someplugin

  $ cv-generator plugins:install someuser/someplugin
```

## `cv-generator plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ cv-generator plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ cv-generator plugins:inspect myplugin
```

## `cv-generator plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ cv-generator plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.

  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.

ALIASES
  $ cv-generator plugins add

EXAMPLES
  $ cv-generator plugins:install myplugin 

  $ cv-generator plugins:install https://github.com/someuser/someplugin

  $ cv-generator plugins:install someuser/someplugin
```

## `cv-generator plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ cv-generator plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.

  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.

EXAMPLES
  $ cv-generator plugins:link myplugin
```

## `cv-generator plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ cv-generator plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ cv-generator plugins unlink
  $ cv-generator plugins remove
```

## `cv-generator plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ cv-generator plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ cv-generator plugins unlink
  $ cv-generator plugins remove
```

## `cv-generator plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ cv-generator plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ cv-generator plugins unlink
  $ cv-generator plugins remove
```

## `cv-generator plugins update`

Update installed plugins.

```
USAGE
  $ cv-generator plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
