# Shoplab Dev Setup

## Get Started

1. Install Linux (if windows)
2. Node, NVM, Git Setup
3. SSH Key Configuration between your machine and github.
4. Pull a master branch that you'll be working with at [Shoplab Repos](https://github.com/orgs/ShopLab-Team/repositories)
5. Checkout to a new branch
6. In the terminal run [npm i] to install dependencies

## Branch Naming Convention

1. Use the prefix ***feat*** when creating a new feature.
2. Use the prefix ***fix*** when fixing a bug.

```bash
# Branch format
feat/[ticket_id]
fix/[ticket_id]

# Ticket id can be found in the jira ticket's url
# e.g. shoplab.atlassian.net/browse/FLASH-11
# the ticket id is "FLASH-11" reference the url above
# feat/flash-11 (feature)
# fix/flash-11  (fix)
```

## Pull Requests (PR)

1. Make sure that the base branch is correct
2. Fill up the pull request template
3. Assign a reviewer

## Creating a dev theme for QA check

1. Run ***shopify theme push -u***
2. In creating a theme, name format should be: **[ticket_name or ticket_id] + Feature name**

```bash
# [FLASH-11] Richtext section
```

## Working on a ticket

[Read here](./ticket.md)

## CSS Guidelines

[Read here](./css-guidelines.md)

## Tech Stack

[Read here](./techstack.md)

## NodeJS Scripting

[Read here](./scripts.md)