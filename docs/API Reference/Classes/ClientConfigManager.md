---
sidebar_position: 3
---

# ClientConfigManager

- Class for instantiating and exporting the Database and library config

## Constructor Parameters

|        Name         |  Type  |                                       Description                                        |      Default       |
| :-----------------: | :----: | :--------------------------------------------------------------------------------------: | :----------------: |
| proceduresDirectory | string | The directory where all your procedures would be read from for generating migration file |    "procedures"    |
| functionsDirectory  | string | The directory where all your functions would be read from for generating migration file  |    "functions"     |
|  triggersDirectory  | string |  The directory where all your triggers would be read from for generating migration file  |     "triggers"     |
| migrationsDirectory | string |                  The directory which houses all of your migration files                  |    "migrations"    |
|   migrationsTable   | string |                 The name of the DB table for keeping track of migrations                 | "other_migrations" |
|       engine        | string |                             The flavour of the SQL database                              |         -          |

## Database Constructor Parameters

- References to the Database connection interfaces of drivers used by the library

  | Engine   | Reference                                                                                               |
  | -------- | ------------------------------------------------------------------------------------------------------- |
  | Postgres | [new CLient](https://node-postgres.com/apis/client#new-client)                                          |
  | MySQL    | [createConnection](https://sidorares.github.io/node-mysql2/docs/examples/connections/create-connection) |
  | MSSQL    | [connect](https://github.com/tediousjs/node-mssql?tab=readme-ov-file#configuration-1)                   |

## Example

```typescript title="config.ts"
import { configDotenv } from "dotenv";
import { ClientConfigManager } from "triprofunc";

configDotenv();

export const configManager = new ClientConfigManager({
  proceduresDirectory: "procedures",
  migrationsDirectory: "migrations",
  functionsDirectory: "functions",
  triggersDirectory: "triggers",
  connectionString: process.env.DATABASE_URL,
  engine: "postgres",
});
```
