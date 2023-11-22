# Borgbackup Ansible Role

This role will install Borgbackup and Borgmatic for Deduplicated Backups.

## User and SSH

The role will add a User named `borgmatic`. \

## Variables
Mandatory Variables:
- `borg_backup_passphrase`

See [ defaults/main.yml ](defaults/main.yml)
