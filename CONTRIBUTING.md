# Contributing Guides to Vibecoders.eu

Thank you for your interest in contributing a guide! Please follow these steps to submit your content via a Pull Request (PR). Submissions must be in Markdown format with specific YAML front matter and placed inside the `/guides/` directory.

## What Can a Guide Include?

Guides should be practical and informative, focusing on tools, stacks, or development practices relevant to the Vibecoders community (EU-focused tech, privacy, open source). Your guide can include text, code snippets, configuration examples, commands, links, and externally hosted images or embedded videos.

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
    * **Write your guide content** below the second `---` using standard Markdown and following the **Guide Content Guidelines** below.
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
    * Edit the file: Fill in the front matter and write your guide content below the second `---` using Markdown, following the **Guide Content Guidelines**.
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

Write your guide content below the second `---` delimiter. Your goal is to create a guide that is clear, accurate, complete, and easy to follow.

* **Structure:** Use a logical flow (Introduction, Prerequisites, Steps, Conclusion). Use Markdown headings (`##`, `###`) for clear sections.
* **Clarity:** Write clear explanations. Explain the *why* behind steps, not just the *how*. Use standard Markdown for lists (`*`, `-`, `1.`), **bold** (`**bold**`), and _italic_ (`_italic_`).
* **Links:** Use standard Markdown links: `[Link description](https://example.com)`. Link to official docs or relevant Vibecoders pages where appropriate.
* **Code Blocks:** Use triple backticks (```) enclosing your code. **Crucially, add a language identifier** right after the opening backticks for syntax highlighting.
    ```bash
    # Example for shell commands
    echo "Hello Vibecoders!"
    npm install cool-package --save-dev
    ```
    ```javascript
    // Example for JavaScript
    function calculate(a, b) {
      // Always test your code
      return a + b;
    }
    ```
    ```json
    // Example for JSON
    { "key": "value", "enabled": true }
    ```
* **Images:** Embed externally hosted images using standard Markdown syntax:
    `![Alt text describing the image](URL_TO_EXTERNALLY_HOSTED_IMAGE)`
    * **Guidelines:** Images **must be hosted externally** (your CDN, Imgur, etc.). **Do not add image files to this repository.** Optimize images (< 300KB recommended). Use meaningful alt text for accessibility. Use images only when they add significant clarity (screenshots, diagrams).
* **Videos:** Embed externally hosted videos (YouTube, Vimeo, Loom recommended) using the HTML `<iframe>` embed code provided by the platform. Paste this code directly into your Markdown file.
    * **Guidelines:** Videos **must be hosted externally**. Ensure the video clearly demonstrates a step or concept that's hard to explain with text alone. *(Note: Embedding requires the Vibecoders.eu site to correctly render iframe tags).*
    * Example `<iframe>` structure (get the actual code from the video platform):
        ```html
        <div style="aspect-ratio: 16 / 9; margin-bottom: 1rem; max-width: 720px;">
          <iframe
            style="width: 100%; height: 100%; border: 0;"
            src="https://www.youtube.com/embed/YOUR_VIDEO_ID"
            title="Video Title For Accessibility"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            allowfullscreen>
          </iframe>
        </div>
        ```
        *(Using a wrapper div with `aspect-ratio` helps maintain video proportions responsively).*
* **Accuracy & Completeness:** Test all commands and code. List all prerequisites. Ensure steps are reproducible. Specify versions if necessary.
* **Proofread:** Check spelling, grammar, and clarity.

## Review Process

* We will review PRs for clarity, accuracy, relevance, formatting, and front matter.
* We may suggest edits via PR comments.
* Ensure content is original or properly attributed. Low quality or out-of-scope submissions may be rejected.

## Licensing

By submitting content via a Pull Request, you agree to license your contribution (the text, code examples, and front matter in the `.md` file) under the terms specified in the [LICENSE](LICENSE) file (e.g., CC-BY-SA 4.0).

## Code of Conduct

(Consider adding a `CODE_OF_CONDUCT.md` file and linking it here).
