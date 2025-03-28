# Contributing Guides to Vibecoders.eu

Thank you for your interest in contributing a guide! Please follow these steps to submit your content via a Pull Request (PR). Submissions must be in Markdown format (`.md`) with specific YAML front matter at the top, and placed inside the `/guides/` directory.

## What Can a Guide Include?

Guides should be practical and informative, focusing on tools, stacks, or development practices relevant to the Vibecoders community (EU-focused tech, privacy, open source). Your guide can include text, code snippets, configuration examples, commands, links, and externally hosted images or embedded videos. See the formatting guidelines below.

## How to Submit

The easiest way is using the GitHub web interface.

**Method 1: Using the GitHub Web Interface (Recommended)**

1.  **Navigate to the Guides Folder:** Go to the `/guides/` folder in this repository: [https://github.com/vibecoders-eu/guides/tree/main/guides](https://github.com/vibecoders-eu/guides/tree/main/guides) *(Ensure this folder exists - you might need to add a placeholder file like `guides/README.md` first).*
2.  **Add File:** Click "Add file" -> "Create new file".
3.  **Name Your File:** In the box after `guides/`, type a filename for your guide. Use a unique slug based on the title, followed by `.md`. Use only lowercase letters, numbers, and hyphens (e.g., `deploying-remix-on-hetzner.md`). The full path should look like `guides/your-guide-slug.md`.
4.  **Add Content:**
    * Copy the structure from `template.md` (located in the root of this repository).
    * Paste it into the editor.
    * **Fill in the YAML front matter** accurately (see requirements below).
    * **Write your guide content** below the second `---` using standard Markdown and following the **Guide Content Guidelines & Formatting** below.
5.  **Propose New File:** Add a commit message (e.g., "Add guide: Deploying Remix on Hetzner") and click "Propose new file".
6.  **Open Pull Request:** Review the details and click "Create pull request".

**Method 2: Using Git Locally (Alternative)**

1.  **Fork & Clone:** Fork this repo, then clone your fork locally.
    ```bash
    git clone [https://github.com/YOUR_USERNAME/guides.git](https://github.com/YOUR_USERNAME/guides.git)
    cd guides
    ```
2.  **Create Branch:**
    ```bash
    git checkout -b add-my-new-guide-title
    ```
3.  **Create & Edit Markdown File:**
    * Ensure a `guides` directory exists (`mkdir guides` if needed).
    * Copy `template.md` into the `guides` directory.
    * Rename it to `guides/your-guide-slug.md`.
    * Edit the file: Fill in the YAML front matter and write your guide content below the second `---`, following the **Guide Content Guidelines & Formatting**.
4.  **Commit Changes:**
    ```bash
    git add guides/your-guide-slug.md
    git commit -m "feat: Add guide '[Your Guide Title]'"
    ```
5.  **Push to Your Fork:**
    ```bash
    git push origin add-my-new-guide-title
    ```
6.  **Open Pull Request:** Go to the main `vibecoders-eu/guides` repo on GitHub and open a PR from your branch.

## Front Matter Requirements

Your Markdown file (`guides/your-guide-slug.md`) **must** start with a YAML front matter block enclosed in `---` delimiters. Please include the following fields:

* **`title`** (Required): The main title of your guide (string).
* **`author_github`** (Required): Your GitHub username (string, no `@`).
* **`description`** (Required): A short (1-2 sentence) summary or excerpt of the guide, used for previews (string, max ~160 chars recommended).
* **`tags`** (Recommended): A list of relevant keywords (lowercase, hyphenated) for categorization (e.g., `["deployment", "database", "remix", "tutorial"]`). Format: `["tag1", "tag2"]`.
* **`level`** (Recommended): Estimated difficulty (`"beginner"`, `"intermediate"`, or `"advanced"`).
* **`related_tools`** (Recommended): A list of tool slugs (from vibecoders.eu) featured in the guide (e.g., `["supabase", "fly-io"]`). Format: `["slug1", "slug2"]`.
* **`vibecoders_stack_url`** (Optional): URL to a relevant stack on vibecoders.eu, if applicable (string).
* **`published_date`** (Optional): The date you originally wrote/published the guide, in `YYYY-MM-DD` format (string). If omitted, we might use the commit date.

Refer to `template.md` for the exact structure.

## Guide Content Guidelines & Formatting

Write your guide content below the second `---` delimiter. Your goal should be to create a guide that is clear, accurate, complete, and easy for others to follow successfully. Aim for a guide so well-structured and detailed that another developer could reliably reproduce your results.

**Structure & Clarity:**

* Follow a logical flow (Introduction, Prerequisites, Steps, Conclusion - see `template.md`).
* Use Markdown headings (`##`, `###`) effectively.
* Write clear explanations. Explain the *why* behind steps, not just the *how*.
* Clearly list any **Prerequisites**.
* Proofread for spelling, grammar, and clarity.

**Formatting Your Content:**

Use standard Markdown and appropriate HTML (for embeds) for readability:

* **Text:** Use standard paragraphs. Use `**bold**` or `_italic_` for emphasis where needed.
* **Lists:** Use bullet points (`*` or `-`) or numbered lists (`1.`, `2.`) for steps or related items.
* **Links:** Use standard Markdown links: `[Link description](https://example.com)`. Link to official documentation or relevant Vibecoders pages when helpful.
* **Code Blocks:** Use triple backticks (```) enclosing your code. **Crucially, add a language identifier** right after the opening backticks for syntax highlighting.
    ```bash
    # Example bash command
    npm install package-name
    ```
    ```javascript
    // Example JavaScript code
    function greet(name) {
      console.log(`Hello, ${name}!`);
    }
    greet('Vibecoder');
    ```
* **Inline Code:** Use single backticks (`) for `variable_names`, `commands`, or filenames within sentences.
* **Images:** Embed externally hosted images using standard Markdown syntax:
    `![Alt text describing the image](URL_TO_EXTERNALLY_HOSTED_IMAGE)`
    * **Guidelines:** Images **must be hosted externally**. **Do not add image files to this repository.** Optimize images (< 300KB suggested). Use descriptive alt text. Use images sparingly, only where they add significant clarity.
* **Videos:** Embed externally hosted videos (YouTube, Vimeo, Loom recommended) using the HTML `<iframe>` embed code provided by the platform. Paste this code directly into your Markdown file.
    * **Guidelines:** Videos **must be hosted externally**. Ensure the video adds significant value. *(Note: Embedding relies on the Vibecoders.eu site correctly processing these iframe tags).*
    * Example `<iframe>` structure (use actual code from video platform):
        ```html
        <div style="aspect-ratio: 16 / 9; margin-bottom: 1rem; max-width: 720px;">
          <iframe
            style="width: 100%; height: 100%; border: 0;"
            src="YOUR_VIDEO_EMBED_URL_HERE"
            title="Video Title For Accessibility"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            allowfullscreen>
          </iframe>
        </div>
        ```
* **Blockquotes:** Use `>` for highlighting notes or quoting text:
    ```markdown
    > **Important:** Always back up your database before performing major upgrades.
    ```
* **Horizontal Rules:** Use `---` on a line by itself to create a visual separator between sections if needed.

**Accuracy & Completeness:**

* **Test everything!** Ensure all commands and code snippets work correctly. Specify versions if critical.
* Include all necessary steps and configuration details.

## Review Process

* We (the maintainers) will review submitted Pull Requests for clarity, accuracy, relevance, formatting, and completeness of front matter.
* We may suggest edits or ask for clarification via PR comments.
* Ensure content is original or properly attributed. Low quality or out-of-scope submissions may be rejected.

## Licensing

By submitting content via a Pull Request, you agree to license your contribution (the text, code examples, and front matter in the `.md` file) under the terms specified in the [LICENSE](LICENSE) file (e.g., CC-BY-SA 4.0).
