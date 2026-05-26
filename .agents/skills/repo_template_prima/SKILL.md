# repo_template_prima Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development conventions and workflows used in the `repo_template_prima` repository. The repository is primarily documentation- and template-oriented, with content and configuration stored in Markdown, YAML, and Bash-oriented files under directories such as `seeds/`, `quests/`, and `guides/`. Use these patterns to keep repository content consistent, readable, and easy to maintain.

## Coding Conventions

### File Naming
- **Pattern:** Descriptive, lowercase, kebab-case names for content and configuration files
- **Example:**  
 ```plaintext
 getting-started.md
 quest-config.yml
 bootstrap.sh
  ```

### Markdown Structure
- **Pattern:** Use clear heading hierarchy, short sections, and fenced code blocks for commands/examples
- **Example:**
 ````markdown
 ## Setup

 Run the following command:

 ```bash
 bash seeds/bootstrap.sh
 ```
 ````

### YAML Style
- **Pattern:** Use consistent indentation and descriptive keys
- **Example:**
 ```yaml
 name: sample-quest
 description: Introductory workflow
 steps:
   - seed-content
   - validate-output
 ```

### Commit Messages
- **Pattern:** Conventional commits with a documentation-oriented prefix when changing guides, templates, or content
- **Example:**
 ```plaintext
 docs: update README with installation instructions
 docs: clarify quest authoring steps
 chore: reorganize template directories
 ```

## Workflows

### Updating Repository Content
**Trigger:** When editing guides, templates, seed content, or repository documentation  
**Command:** `/docs-update`

1. Make your Markdown, YAML, or shell-script changes.
2. Review formatting, links, and indentation for consistency.
3. Stage the changes:
  ```bash
  git add .
  ```
4. Commit using a conventional message:
  ```bash
  git commit -m "docs: update guide wording"
  ```
5. Push your changes:
  ```bash
  git push
  ```

## Validation Patterns

- **Primary checks:** Verify Markdown formatting, YAML structure, and shell command accuracy
- **File patterns:** Content is commonly stored in `.md`, `.yml`/`.yaml`, and `.sh` files
- **Examples:**
 ```plaintext
 guides/getting-started.md
 seeds/packages.yaml
 seeds/bootstrap.sh
 ```
- **Typical validation tasks:**
 ```bash
 bash -n seeds/bootstrap.sh
 ```

## Commands
| Command      | Purpose                                                   |
|--------------|-----------------------------------------------------------|
| /docs-update | Update repository documentation, templates, and content   |
