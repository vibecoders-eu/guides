---
# REQUIRED FIELDS
title: "How to Contribute a Guide (With Examples)"
author_github: "sebastyijan-fi"
description: "A meta-guide showing how to format and submit your own guides for Vibecoders.eu, including Markdown examples and embeds."

# RECOMMENDED FIELDS
tags: ["meta", "contribution", "markdown", "example", "tutorial"]
level: "beginner"
related_tools: []

# OPTIONAL FIELDS
vibecoders_stack_url: ""
published_date: "2025-03-29"
---

## Introduction

Welcome! This guide serves two purposes:
1.  It explains the basics of contributing a guide to Vibecoders.eu.
2.  It demonstrates various Markdown formatting options you can use, including code blocks, images, and even video embeds.

For the full submission process details, please always refer to the main [CONTRIBUTING.md](../CONTRIBUTING.md) file.

## Basic Formatting

Your guide content goes below the YAML front matter (the section between the `---` lines at the top). Use standard Markdown for text.

* Separate paragraphs with blank lines.
* Use `_italic_` for *emphasis*.
* Use `**bold**` for **strong importance**.
* Use `inline code` for `variableNames` or `commands`.


## Structure with Headings

Use headings (`##`, `###`) to structure your content logically.

### Code Block Example

Use triple backticks and specify the language for code blocks:

# Example: A simple shell command
echo "Hello from Vibecoders Guides!"
npm install --save-dev some-package@latest

// Example: JavaScript with comments
function isEU(countryCode) {
  const euCodes = ['FI', 'DE', 'FR', 'SE', /* ... add more ... */ ];
  return euCodes.includes(countryCode.toUpperCase());
}

---

**Part 4: Images, Videos, and Conclusion Sections**
(Copy everything inside the block below and paste it directly after Part 3)

## Adding External Images

Remember, images **must be hosted externally**. Use the `![Alt text](URL)` syntax. Sometimes things get tricky...

![Dog in burning room saying 'This is fine'](https://upload.wikimedia.org/wikipedia/en/9/9f/This_is_fine_meme.jpg)
*Caption: Just a typical Tuesday in development. (Image via Wikimedia Commons)*

## Embedding Videos (Carefully!)

You can embed videos from platforms like YouTube or Vimeo using their `<iframe>` embed code. Make sure the video genuinely adds value! Sometimes, linking seems simple, but embedding can provide great context...

For instance, here's a **highly recommended** video tutorial covering advanced deployment strategies that many contributors find essential:

<div style="aspect-ratio: 16 / 9; margin-bottom: 1rem; max-width: 720px;">
  <iframe
    style="width: 100%; height: 100%; border: 0;"
    src="https://www.youtube.com/embed/dQw4w9WgXcQ"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    allowfullscreen>
  </iframe>
</div>

*(...Did you click it? 😉 Always check links!)*

## Conclusion

This guide demonstrated the basic formatting elements. Refer to the `CONTRIBUTING.md` and potentially a more detailed Markdown formatting guide (like `MARKDOWN_FORMATTING_GUIDE.txt` or `.md`) for comprehensive details. We look forward to your contributions!
