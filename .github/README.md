# ans_role_config_boot_messages

Configure persistent system bootup messages.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_boot_messages.svg?label=release)](https://github.com/digimokan/ans_role_config_boot_messages/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.txt "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Requirements](#requirements)
* [Quick Start](#quick-start)
    * [Use From Playbook](#use-from-playbook)
* [Role Options](#role-options)
* [Contributing](#contributing)

## Purpose

* Configure system bootup to retain all messages, errors, etc on the screen.

## Supported Operating Systems

* Arch Linux.

## Requirements

* GRUB.

## Quick Start

### Use From Playbook

1. Create `requirements.yml` in ansible project root, and add this content:

   ```yaml
   # requirements.yml
   - src: https://github.com/digimokan/ans_role_config_boot_messages
   ```

2. From the project root directory, install/download the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles --force-with-deps
   ```

   * _NOTE:_ `--force-with-deps` _ensures subsequent calls download updates_

3. Include the role like any local role, from the project playbook:

   ```yaml
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Configure persistent system bootup messages"
         ansible.builtin.include_role:
           name: ans_role_config_boot_messages
   ```

## Role Options

Define these _required_ vars for the role:

  * `user_name`: user login name to configure the XDG user dirs for

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_boot_messages/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

