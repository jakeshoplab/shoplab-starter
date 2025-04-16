# Pushing Testing Theme to Shopify Store

## 🆕 If the Theme Is Newly Created

```bash
  shopify theme push -u -x .shopifyignore
```

### Then specify theme name with this format

> [ticket_id] Description

```bash
  [SCM-3] Small Topbar update
```

## 🎯Targeting a Specific Theme (If Theme Existed)

### Theme Name

```bash
  shopify theme push --theme "[SCM-3] Small Topbar update" -u -x .shopifyignore
```

### Theme ID

```bash
  shopify theme push --theme-id=123456789 -u -x .shopifyignore
```

## 📋 List Available Themes

To view all available themes and their IDs:

```bash
shopify theme list
```

## 🔖 Command Flags Reference

1. -u or --unpublished (theme as unpublished)
2. -x or --ignore-file file_name (files to ignore when executing a command)