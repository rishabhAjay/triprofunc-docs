---
sidebar_position: 2
---

# Initial Setup

- To install the package, you can either use npm (`npm i triprofunc`) or yarn (`yarn add triprofunc`)

- Next, you will have to specify a _config file_ either in **JS** or **TS**. The `ClientConfigManager` needs to be instantiated and name exported. For example:

```javascript title="config.js"
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

- The library currently supports three flavours of SQL: `postgres`, `mysql` and `mssql`. You can choose
  from either of these as the `engine` parameter in the config

- Furthermore, the library uses the [pg](https://www.npmjs.com/package/pg) package for postgres, the [mysql](https://www.npmjs.com/package/mysql2) package for mysql and the [mssql](https://www.npmjs.com/package/mssql) package as the underlying drivers for interacting with the DB. Please refer to the package docs for connection parameters depending on the type of SQL Database

- If you are using Typescript, the `ClientConfigManager` class is typed to switch to different driver interfaces depending on the engine you choose

- And that is it for the setup
