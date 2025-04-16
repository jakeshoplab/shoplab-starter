# Shopify Theme Development Guide

## Working On A Ticket

1. Review ticket title and description
2. If requested an estimation, place your estimate on the comment section and on the “Estimations” tab, fill the Estimation Accuracy, Estimate complexity, and Estimate risk. Once the PM approved it, you can now start working on it.

## Get Started

1. Clone the **master** branch from [Shoplab Repos](https://github.com/orgs/ShopLab-Team/repositories) to start working.
2. Navigate into the cloned repository.
3. Open your terminal and run the following commands:

    ```bash
    # Install dependencies (if any)
    npm install

    # Pull the latest Shopify theme files (with authentication)
    shopify theme pull -l -n -o settings_data.json templates/*.json sections/*.json --store store_domain.myshopify.com

    # Pull the latest Shopify theme files (without authentication)
    shopify theme pull -l -n -o settings_data.json templates/*.json sections/*.json
    ```

4. Create a new Git branch — see the [naming convention guide](./naming-branch-convention.md).
5. Run the theme locally:

    ```bash
    shopify theme dev -s shop_domain.myshopify.com
    ```

## ✅ After Development

- Push your updated theme to the Shopify store — this also serves as the QA version for inspection.
  → [Follow the guide here](./shopify-pushing-theme.md)

- Go to the **Themes** section in Shopify to locate and inspect your newly pushed theme.

- Once everything looks good:
  - `git add`, `commit`, and `push` your branch  
  → [Refer to the commit writing guide](./writing-a-commit.md)

- Visit the GitHub repo and submit a **Pull Request (PR)**.

- When creating the PR, fill in all required fields.  
  - If the PR template doesn’t appear, include the **Jira Ticket URL** in the PR description.

- After submitting the PR, return to the Jira ticket and leave a completion comment.  
  → [Follow this guide](./jira.md)
