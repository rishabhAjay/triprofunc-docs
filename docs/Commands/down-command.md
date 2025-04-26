---
sidebar_position: 4
---

# The down command

- This command reverts the latest migration changes and removes the record from the migrations table

## Command Info

- Run `triprofunc --config config.js down`

  - `--config` is the config file you pass

## Notes

- The command will revert only the latest run migration.

- The command runs anything that comes after the DOWN marker in the file

- A record is deleted of the latest run migration from the migrations table depicting a successful revert
