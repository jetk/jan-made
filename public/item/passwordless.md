# passwordless-sqlite

## Why
I was building a side project where privacy was a high priority so we decided I should build our own authentication. I chose a magic-link authentication UX pattern because I liked the balance of security and ease, but could not find a Passwordless library for the database we were using, sqlite. Because we were bound to sqlite for other purposes, I decided to implement the library myself.

## What
passwordless-sqlite is a provides a secure token storage for Passwordless, a node.js module for Express that allows website authentication without password using verification through email or other means. Passwordles-sqlite is also implemented in node.js

## How
I was fortunate enough to find a MySQL implementation of the token store which itself had been cribbed from a Postgres implementation. By translating what I knew of MySQL's interfaces to what I knew about sqlite, I was able to port the token store.


## Outcome
Passwordless-sqlite was published to the [NPM registry](https://www.npmjs.com/package/passwordless-sqlite) and has since been download a few hundred times
