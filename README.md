# Borgbackup Ansible Role

This role will install Borgbackup and Borgmatic for Deduplicated Backups.

## User and SSH

The role will add a User named `borgmatic`. \

## Variables
Mandatory Variables:
- `borg_backup_passphrase`

See [ defaults/main.yml ](defaults/main.yml)

## pipx Upgrade Workaround (Ubuntu 24.04)

If pipx <1.7 is detected on Ubuntu 24.04, the role applies a workaround to upgrade pipx and ensure global install works as expected. This workaround is only applied on Ubuntu systems.

**Note:** Molecule tests on macOS/Homebrew do not trigger this workaround and may fail if pipx is not installed globally. For production, this role is intended for Ubuntu/apt environments.

See `tasks/force_update_pipx.yml` for details.
