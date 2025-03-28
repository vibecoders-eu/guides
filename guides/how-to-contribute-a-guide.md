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
published_date: "2025-03-28"
---


INTRODUCTION

Welcome! This guide serves two purposes:
1.  It explains the basics of contributing a guide to Vibecoders.eu.
2.  It demonstrates various Markdown formatting options you can use, including code blocks, images, and even video embeds.

For the full submission process details, please always refer to the main CONTRIBUTING.md file (../CONTRIBUTING.md).


BASIC FORMATTING

Your guide content goes below the YAML front matter (the section between the `---` lines at the top). Use standard Markdown for text.

* Separate paragraphs with blank lines.
* Use _italic_ for *emphasis*.
* Use *bold* for *strong importance*.
* Use `inline code` for `variableNames` or `commands`.


STRUCTURE WITH HEADINGS

Use headings like this (in the .md file, you'd use ##, ### etc.) to structure your content logically.

CODE BLOCK EXAMPLE

Use indentation for code blocks in this text view. In your actual .md file, use triple backticks ``` with language identifiers.

Example bash command:

  # Example: A simple shell command
  echo "Hello from Vibecoders Guides!"
  npm install --save-dev some-package@latest

Example JavaScript:

  // Example: JavaScript with comments
  function isEU(countryCode) {
    const euCodes = ['FI', 'DE', 'FR', 'SE', /* ... add more ... */ ];
    return euCodes.includes(countryCode.toUpperCase());
  }


ADDING EXTERNAL IMAGES

Remember, images *must be hosted externally*. Use the ![Alt text](URL) syntax in your .md file.

Image Example (Syntax in .md):
  ![Placeholder image showing a 600x400 box with text](https://via.placeholder.com/600x400.png?text=Example+Image+(Externally+Hosted))

Caption: A placeholder image loaded from via.placeholder.com.


EMBEDDING VIDEOS (CAREFULLY!)

You can embed videos from platforms like YouTube or Vimeo using their <iframe> embed code in your .md file. Make sure the video genuinely adds value! Sometimes, linking seems simple, but embedding can provide great context...

For instance, here's a *highly recommended* video tutorial covering advanced deployment strategies that many contributors find essential (Syntax for .md file):

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

(...Did you click the link when viewing the rendered version? 😉 Always check links!)


CONCLUSION

This guide demonstrated the basic formatting elements. Refer to the CONTRIBUTING.md and potentially a more detailed Markdown formatting guide (like MARKDOWN_FORMATTING_GUIDE.txt or .md) for comprehensive details. We look forward to your contributions!

---
(Context: Helsinki, Finland - Friday, March 28, 2025 at 12:42 PM)
