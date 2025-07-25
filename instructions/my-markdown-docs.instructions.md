---
description: "Comprehensive documentation and Markdown content creation standards"
applyTo: "**/*.md"
---

# Comprehensive Markdown Documentation Instructions

These are our comprehensive documentation writing and Markdown formatting guidelines combining style, structure, and technical requirements.

## General Writing Style

- Get to the point fast.
- Talk like a person.
- Simpler is better.
- Be brief. Give customers just enough information to make decisions confidently. Prune every excess word.

## Grammar and Voice

- Use present tense verbs (is, open) instead of past tense (was, opened).
- Write factual statements and direct commands. Avoid hypotheticals like "could" or "would".
- Use active voice where the subject performs the action.
- Write in second person (you) to speak directly to readers.
- Use gender-neutral language.
- Avoid multiple -ing words that can create ambiguity.
- Keep prepositional phrases simple and clear.
- Place modifiers close to what they modify.

## Capitalization

- Use sentence-style capitalization for everything except proper nouns.
- Always capitalize proper nouns.
- Don't capitalize the spelled-out form of an acronym unless it's a proper noun.
- Use title-style capitalization for product and service names.
- In programming languages, follow the traditional capitalization of keywords and other special terms.
- Don't use all uppercase for emphasis.

## Numbers

- Spell out numbers for zero through nine, unless space is limited. Use numerals for 10 and above.
- Spell out numbers at the beginning of a sentence.
- Spell out ordinal numbers such as first, second, and third. Don't add -ly to form adverbs from ordinal numbers.

## Punctuation

- Use short, simple sentences.
- End all sentences with a period.
- Use one space after punctuation marks.
- After a colon, capitalize only proper nouns.
- Avoid semicolons - use separate sentences instead.
- Use question marks sparingly.
- Don't use slashes (/) - use "or" instead.

## Markdown Structure and Formatting

### Headings

- Use appropriate heading levels (H2, H3, etc.) to structure your content.
- Do not use an H1 heading, as this will be generated based on the title.
- Use `##` for H2 and `###` for H3. Ensure that headings are used in a hierarchical manner.
- Recommend restructuring if content includes H4, and more strongly recommend for H5.
- Don't apply an inline style like italic, bold, or inline code style to headings.

### Lists

- Use bullet points or numbered lists for lists. Ensure proper indentation and spacing.
- Use `-` for bullet points and `1.` for numbered lists.
- Indent nested lists with two spaces.

### Code Blocks and Code Elements

- Use fenced code blocks for code snippets. Specify the language for syntax highlighting.
- Use triple backticks (```) to create fenced code blocks.
- Specify the language after the opening backticks for syntax highlighting (e.g., ```csharp).
- Use code style for:
  - Code elements, like method names, property names, and language keywords.
  - SQL commands.
  - NuGet package names.
  - Command-line commands.
  - Database table and column names.
  - Resource names (like virtual machine names) that shouldn't be localized.
  - URLs that you don't want to be selectable.
- For code placeholders, if you want users to replace part of an input string with their own values, use angle brackets (less than < and greater than > characters) on that placeholder text.

### Text Formatting

- UI elements, like menu items, dialog names, and names of text boxes, should be in **bold** text.
- Use proper markdown syntax for emphasis and formatting.

### Links

- Use proper markdown syntax for links. Ensure that links are valid and accessible.
- Use `[link text](URL)` for links. Ensure that the link text is descriptive and the URL is valid.
- Links to other documentation articles should be relative, not absolute. Start relative links with `/docs/` and include the `.md` suffix.
- Links in release notes should be full URLs, not relative. Use the `https://code.visualstudio.com/docs/` domain.
- Links to bookmarks within the same article should be relative and start with `#`.
- Link descriptions should be descriptive and make sense on their own. Don't use "click here" or "this link" or "here".

### Images

- Use images only when they add value.
- Use proper markdown syntax for images. Include alt text for accessibility.
- Use `![alt text](image URL)` for images. Include a brief description of the image in the alt text.
- Images have a descriptive and meaningful alt text that starts with "Screenshot showing" and ends with ".".
- Videos have a descriptive and meaningful alt text or title that starts with "Video showing" and ends with ".".

### Tables

- Use markdown tables for tabular data. Ensure proper formatting and alignment.
- Use `|` to create tables. Ensure that columns are properly aligned and headers are included.

### Line Length and Whitespace

- Limit line length to 400 characters for readability.
- Break lines at 80 characters to improve readability. Use soft line breaks for long paragraphs.
- Use appropriate whitespace to separate sections and improve readability.
- Use blank lines to separate sections and improve readability. Avoid excessive whitespace.

## Alerts and Special Content

- Alerts are a Markdown extension to create block quotes that render with colors and icons that indicate the significance of the content. The following alert types are supported:
  - `[!NOTE]` Information the user should notice even if skimming.
  - `[!TIP]` Optional information to help a user be more successful.
  - `[!IMPORTANT]` Essential information required for user success.
  - `[!CAUTION]` Negative potential consequences of an action.
  - `[!WARNING]` Dangerous certain consequences of an action.

## Numbered Steps and Procedures

- Write complete sentences with capitalization and periods
- Use imperative verbs
- Clearly indicate where actions take place (UI location)
- For single steps, use a bullet instead of a number
- When allowed, use angle brackets for menu sequences (File > Open)

## Terminology and Word Choice

- Use "Select" instead of "Click" for UI elements like buttons, menu items, links, dropdowns, and checkboxes.
- Use "might" instead of "may" for conditional statements.
- Avoid latin abbreviations like "e.g.". Use "for example" instead.
- Use the verb "to enable" instead "to allow" unless you're referring to permissions.
- Follow the terms and capitalization guidelines in the VS Code docs wiki.

## Front Matter and Metadata Requirements

Include YAML front matter at the beginning of the file with required metadata fields:

- `post_title`: The title of the post.
- `author1`: The primary author of the post.
- `post_slug`: The URL slug for the post.
- `microsoft_alias`: The Microsoft alias of the author.
- `featured_image`: The URL of the featured image.
- `categories`: The categories for the post. These categories must be from the list in /categories.txt.
- `tags`: The tags for the post.
- `ai_note`: Indicate if AI was used in the creation of the post.
- `summary`: A brief summary of the post. Recommend a summary based on the content when possible.
- `post_date`: The publication date of the post.

## Validation and Quality Assurance

- Ensure that the content follows the markdown content rules specified above.
- Ensure that the content is properly formatted and structured according to the guidelines.
- Run the validation tools to check for compliance with the rules and guidelines.
- Validate that all links are functional and accessible.
- Verify that all code blocks have appropriate language specifications.
- Confirm that all images have descriptive alt text.
