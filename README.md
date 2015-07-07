# Ansible Role: oh-my-zsh

Installs and configures the zsh shell and oh-my-zsh.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    ohmyzsh_copy_zshrc: true

Whether to set copy a .zshrc file. This can be set to `false` if you already have your own copy.

    ohmyzsh_change_shell: true

Whether to change the default shell for the specified user accounts.

    ohmyzsh_users: []

A list of user accounts to update.

    ohmyzsh_path: ~/.oh-my-zsh

Where to install oh-my-zsh.

    ohmyzsh_theme: robbyrussell

Which theme to use.

    ohmyzsh_aliases: []

Any aliases to add to the bottom of `.zshrc`.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - { role: oh-my-zsh, ohmyzsh_users: [ vagrant ] }
