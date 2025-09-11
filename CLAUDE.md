# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository manages technical articles for Zenn publication using Zenn CLI. Articles are written in Markdown format with frontmatter metadata and can be previewed locally before publication.

## Repository Structure

```
.
├── articles/           # Article files (.md files with frontmatter)
├── books/             # Book files (book-format content)
├── package.json       # Project configuration
└── node_modules/      # Dependencies (includes zenn-cli)
```

## Essential Commands

### Content Management
```bash
# Preview content locally in browser
npx zenn preview

# Create new article
npx zenn new:article

# Create new book
npx zenn new:book

# List all articles
npx zenn list:articles

# List all books
npx zenn list:books
```

### Development
```bash
# Install dependencies
npm install
```

## Content Structure

### Articles
- Located in `articles/` directory
- Markdown files with frontmatter containing:
  - `title`: Article title
  - `emoji`: Display emoji
  - `type`: "tech" or "idea"
  - `topics`: Array of topic tags
  - `published`: Boolean publication status

### Example Article Frontmatter
```yaml
---
title: "Article Title"
emoji: "🤔"
type: "tech"
topics: ["go", "golang"]
published: true
---
```

## Git Workflow and Commit Conventions

- Repository is integrated with GitHub for Zenn publication
- Always confirm commit plans before executing
- Use `docs:` prefix for documentation changes
- Commit changes with appropriate granularity and descriptive messages

## Architecture Notes

This is a content-focused repository using Zenn CLI for:
- Local content preview via built-in server
- Content validation and formatting
- Integration with Zenn's publication platform
- Markdown processing with Zenn-specific features