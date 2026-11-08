# claude-algolia-search-skill

A Claude Code skill for implementing, configuring, and improving search experiences with Algolia.

## Overview

This skill covers the application-side patterns needed to build useful search experiences. It helps connect an application to an Algolia index, implement interactive search interfaces, tune relevance, configure filters, and support search workflows in modern web applications.

## Main Capabilities

- Configure search clients and index access.
- Design indexing and record structures.
- Implement search interfaces.
- Build type-ahead and instant search experiences.
- Add filters, facets, and pagination.
- Tune relevance and ranking.
- Support frontend integrations such as React InstantSearch.
- Consider server-side rendering where required.
- Review search performance and result quality.

## Installation

Install the packages required by the project and clone the skill:

```bash
git clone https://github.com/Brajesh31/claude-algolia-search-skill.git ~/.claude/skills/algolia-search
```

A typical JavaScript application uses the Algolia search client and the UI integration appropriate to its framework. Check the installed package versions before applying examples.

## Usage

Invoke the skill when adding or improving search:

```text
/algolia-search
```

Provide the frontend framework, index structure, searchable attributes, filter requirements, expected result volume, and relevance goals.

## Search Implementation Workflow

1. Define the search use case and expected user behavior.
2. Design index records around the fields users need to search and filter.
3. Configure the client using environment-based credentials.
4. Build the search input and result interface.
5. Add facets, filters, sorting, and pagination where appropriate.
6. Tune searchable attributes and ranking.
7. Test representative queries and edge cases.
8. Measure latency and relevance.
9. Review access controls and exposed credentials before deployment.

## React InstantSearch Concepts

Common interface building blocks include:

- Search box for query input.
- Hits for result rendering.
- Refinement lists for facet filters.
- Pagination for navigating result pages.
- Search state for coordinating widgets.
- Custom result components for product-specific presentation.

Choose components based on the interaction required. Avoid adding widgets that do not support a real user need.

## Relevance and Indexing Checklist

- Records contain stable identifiers.
- Searchable attributes reflect user intent.
- Attribute ranking is deliberate.
- Facets are configured for actual filter needs.
- Synonyms and typo tolerance are evaluated with real queries.
- Index updates are repeatable.
- Result ranking is reviewed with representative test cases.
- Empty and no-result states are designed.

## Security Checklist

- Do not expose admin API keys in browser code.
- Use the least-privileged key suitable for the client.
- Restrict keys where supported.
- Keep index configuration changes controlled.
- Validate user-controlled filters and query parameters.

## Repository Contents

- `SKILL.md`: Main Algolia search instructions.
- `README.md`: Search architecture, implementation workflow, and quality checklist.

## Practical Guidance

A working search box is not enough. Evaluate whether users can find the right records, understand why results appear, refine the result set, and recover when no matches are found.
