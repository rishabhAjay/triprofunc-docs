---
sidebar_position: 3
---

# The up command

- This command applies the new changes to the database and adds the migration to the migrations table

## Command Info

- Run `triprofunc --config config.js up`

  - `--config` is the config file you pass

## Notes

- The command will run all the pending migrations available in the migrations directory.

- The command runs anything that comes after the UP marker and before the DOWN marker in the file

- A record is inserted of every new migration to the migrations table depicting a successful run
