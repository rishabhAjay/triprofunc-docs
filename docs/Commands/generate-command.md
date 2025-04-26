---
sidebar_position: 1
---

# The generate command

- This command auto-generates all the **triggers, procedures and functions** for you in SQL files and dumps it in the folder you specify

## Command Info

- Run `triprofunc --config config.js generate <folder_name>`

  - `--config` is the config file you pass
  - `<folder_name>` is the folder in which you want the SQL files in

## Notes

- The sql files generated will be in their own folders(_triggers_, _procedures_ and _functions_)

- The sql files will be named according to the name of the given SQL trigger/procedure/function

- For postgres since there is a possibility of having the _same trigger name for multiple tables_,
  `_tablename` would be appended to the filename
