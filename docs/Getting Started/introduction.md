---
slug: /
sidebar_position: 1
---

# Introduction

- **TriProFunc** is a library to help manage the other parts of your Database like Triggers, Procedures and Functions. It currently supports the aforementioned Database objects but more could be added in future(Views for example). It also currently supports Postgres, MySQL and MSSQL.

## Features

- Centralized JS/TS based instantiation

- Support for **Postgres**,**MySQL** and **Microsoft SQL Server**

- Auto-generates SQL Triggers, Procedures and Functions for an existing project

- Auto-generates migration changes

- Typescript support

- Customizable configuration

- Ease of running and rolling back migrations

- Colour-coded terminal output

## Requirements

- You need to have **Docker installed on your machine**. This is because the migrations are generated based on a lightweight container of the Database engine you are using and the diff in your migration is computed with it. There weren't any ready-to-use parsers for Triggers, Procedures and Functions so docker is the only major dependency

## Notes

- This library _has not been tested against all and old versions_ of the given Database engine. If for some reason you face difficulties integrating this library with your version of the Database, please reach out via [Discussions](https://google.com)

## Contact

- If you have further queries, you can contact me on the email [triprofunc@proton.me](mailto:triprofunc@proton.me)
