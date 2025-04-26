---
sidebar_position: 2
---

# The migrate command

- This command auto-generates migration files based on the changes you have made relative to the previous state of the queries

## Command Info

- Run `triprofunc --config config.js migrate <migration_name>`

  - `--config` is the config file you pass
  - `<migration_name>` is name of the migration file generated

## Notes

- The migration file generated will have the latest changes of triggers, procedures and functions all combined into one. The migration file is an SQL file

- The migration file generated has two markers, an **UP** section that contains the new changes and the **DOWN** section for the current changes. It is suggested to not change these files or the markers

- Since MySQL and MSSQL do not support the `CREATE OR REPLACE` syntax, the objects would be dropped and then created. This is exempted for Postgres as it supports the aforementioned syntax.
