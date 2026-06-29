# Mintlify documentation

## Working relationship
- You can push back on ideas-this can lead to better documentation. Cite sources and explain your reasoning when you do so
- ALWAYS ask for clarification rather than making assumptions
- NEVER lie, guess, or make up anything

## Project context
- Format: MDX files with YAML frontmatter
- Config: docs.json for navigation, theme, settings
- Components: Mintlify components

## Audience & altitude
- These docs are for the people who **use and administer** Nobly Insight — customers, super-users, and consultants — not for operators who deploy or configure the environment.
- Write at **product altitude**: document what a user or administrator does in the product UI, and the concepts they need to succeed.
- Do NOT document environment/deployment internals — connection strings, configuration keys, feature-flag identifiers, environment variables, database logins, migrations, background-worker switches, timeout settings. If it is "taken care of by setting up the environment," it does not belong here.
- A setup page, when needed, stays at **admin altitude**: what an administrator enables and grants inside the product (e.g. "the feature is provisioned per tenant; grant these permissions"). Mirror `retention/setup.mdx` for depth and tone.

## Content strategy
- Document just enough for user success - not too much, not too little
- Prioritize accuracy and usability
- Make content evergreen when possible
- Search for existing content before adding anything new. Avoid duplication unless it is done for a strategic reason
- Check existing patterns for consistency
- Start by making the smallest reasonable changes

## docs.json

- Refer to the [docs.json schema](https://mintlify.com/docs.json) when building the docs.json file and site navigation

## Frontmatter requirements for pages
- title: Clear, descriptive page title
- description: Concise summary for SEO/navigation

## Writing standards
- Second-person voice ("you")
- Prerequisites at start of procedural content
- Test all code examples before publishing
- Match style and formatting of existing pages
- Include both basic and advanced use cases
- Language tags on all code blocks
- Alt text on all images
- Relative paths for internal links
- Describe who can do something by the **permission it requires**, not by a job title. A capability is open to anyone holding the permission — a customer administrator, super-user, or consultant — so never write "this page is for consultants." Mirror the permission-based language in the Permissions & access section.

## Git workflow
- NEVER use --no-verify when committing
- Ask how to handle uncommitted changes before starting
- Create a new branch when no clear branch exists for changes
- Commit frequently throughout development
- NEVER skip or disable pre-commit hooks

## Terminology
- NEVER write "OnBase" in documentation — always use "Nobly Insight". This covers prose, headings, captions, alt text, and sample data.
- Screenshots must not show "OnBase" either. Before adding one, check the nav, chrome, helper text, and sample data; if the live product still shows "OnBase", re-capture after the string is fixed or crop it out — never commit an image showing "OnBase".
- If "OnBase" appears in the live product (a UI string or a required identifier), don't silently rename it in the docs — that misrepresents the product. Flag it so the product string can be fixed, and keep it out of screenshots meanwhile.

## Do not
- Skip frontmatter on any MDX file
- Use absolute URLs for internal links
- Include untested code examples
- Commit screenshots or images that show "OnBase" or other legacy branding
- Make assumptions - always ask for clarification
