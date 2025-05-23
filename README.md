# 🌱 The Foost Digital Garden 🍲✍️

Welcome to **The Foost Digital Garden**! This is our community's shared space for cultivating knowledge, creativity, and connection. Think of it as a living, breathing collection of recipes, blog posts, poems, thoughts, and more, all nurtured by us, for us.

This repository is built using [Obsidian](https://obsidian.md), a powerful knowledge base that works on local Markdown files. Our goal is to integrate this digital garden with our main Foost website, making our collective creations accessible to everyone.

## 🌳 What is a Digital Garden?

Unlike a traditional blog, a digital garden is a more fluid and interconnected space. Notes can be in various stages of completion ("seedlings," "budding," "evergreen"), and they are often linked together to create a web of knowledge. It's less about polished, finished pieces and more about learning, sharing, and growing ideas in public.

## 🌟 What You'll Find Inside

This garden is home to a diverse range of content, including (but not limited to!):

*   🍳 **Recipes:** Delicious dishes, cooking tips, and kitchen experiments.
*   ✍️ **Blog Posts:** Thoughts, articles, and reflections on various topics.
*   📜 **Poems & Creative Writing:** Original works of art from our community.
*   💡 **Ideas & Notes:** Sparks of inspiration, interesting links, and developing thoughts.
*   📚 **Book Summaries/Reviews:** What we're reading and learning.
*   ...and anything else our community wishes to share and grow!

## 🛠️ How It Works

1.  **Obsidian:** We use Obsidian to write, organize, and link our notes locally. It's free and works with plain Markdown files.
2.  **GitHub:** This repository acts as the central hub for all our garden's content. We use Git for version control and collaboration.
3.  **Website Integration:** The content from this repository will be (or is being) processed and displayed on The Foost website, making it easily accessible and searchable.

## 🚀 Getting Started & Contributing

We'd love for you to contribute! Here's how:

### 1. Prerequisites

*   **Git:** You'll need Git installed on your computer. [Learn Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
*   **Obsidian (Recommended):** Download and install [Obsidian](https://obsidian.md/download). While you can edit Markdown files with any text editor, Obsidian makes linking and organization much easier.
*   **GitHub Account:** You'll need a GitHub account.

### 2. Setting Up Your Local Environment

1.  **Fork this Repository:** Click the "Fork" button at the top right of this page to create your own copy.
2.  **Clone Your Fork:**
    ```bash
    git clone https://github.com/YOUR_USERNAME/the-foost-digital-garden.git
    cd the-foost-digital-garden
    ```
3.  **Open in Obsidian:**
    *   Open Obsidian.
    *   Click "Open folder as vault."
    *   Select the `the-foost-digital-garden` folder you just cloned.

### 3. Contribution Guidelines

We want to keep our garden organized and easy to navigate.

*   **File Naming:**
    *   Use descriptive, lowercase filenames with hyphens instead of spaces (e.g., `my-amazing-vegan-chili.md`).
    *   Avoid special characters.
*   **Folder Structure:**
    *   Place your files in the appropriate top-level folder:
        *   `recipes/`
        *   `blog/`
        *   `poems/`
        *   `notes/` (for general notes, ideas, etc.)
        *   `assets/images/` (for all images used in your notes - create subfolders here if needed, e.g., `assets/images/recipes/`)
    *   If you're unsure, ask! Or create a new folder if it makes sense for a new category.
*   **Markdown & Frontmatter:**
    *   All content should be in Markdown (`.md`) format.
    *   **Crucial:** Add YAML frontmatter at the very top of each file. This metadata helps us categorize and display content on the website.
        ```yaml
        ---
        title: "My Awesome Recipe Title"
        date: YYYY-MM-DD # Date of creation or last significant update
        author: "Your Name/Nickname"
        tags: [recipe, vegan, quick, dinner] # Relevant tags, lowercase
        # Optional:
        # status: seedling # (e.g., seedling, budding, evergreen) - helps show how developed an idea is
        # publish: true # (default is true, set to false if it's a draft not ready for the website yet)
        ---

        Your amazing content starts here...
        ```
*   **Linking:**
    *   Use Obsidian's internal linking syntax `[[Note Title]]` to link between notes within the garden.
    *   For external links, use standard Markdown: `[Link Text](https://example.com)`.
*   **Images:**
    *   Place images in the `assets/images/` folder (or a relevant subfolder).
    *   Link to them using relative paths: `![Image Alt Text](../../assets/images/your-image.jpg)` (adjust `../` as needed based on your note's location).
    *   Keep image file sizes reasonable.

### 4. Submitting Your Contributions

1.  **Create a New Branch:**
    ```bash
    git checkout -b your-feature-or-note-name
    ```
2.  **Add Your Files:** Create your new `.md` files, add images, and make your edits.
3.  **Commit Your Changes:**
    ```bash
    git add .
    git commit -m "feat: Add new recipe for vegan chili"
    # Or "docs: Update contribution guidelines"
    # Or "fix: Correct typo in poem"
    ```
    (Try to follow [Conventional Commits](https://www.conventionalcommits.org/) if possible!)
4.  **Push to Your Fork:**
    ```bash
    git push origin your-feature-or-note-name
    ```
5.  **Open a Pull Request (PR):**
    *   Go to your fork on GitHub (`https://github.com/YOUR_USERNAME/the-foost-digital-garden`).
    *   You should see a prompt to "Compare & pull request." Click it.
    *   Write a clear title and description for your PR, explaining your changes.
    *   Submit the PR!

A community member will review your contribution, provide feedback if necessary, and merge it.

## 🌐 Website Integration (The Vision)

This Obsidian vault serves as the "source of truth" for a section of The Foost website. A static site generator or a custom script will periodically (or on new commits) read the Markdown files from this repository, process the frontmatter, and render them as HTML pages on our live website. This ensures our shared knowledge is always up-to-date and beautifully presented.

*(More technical details about the specific integration method can be added here once decided/implemented.)*

## 💬 Community & Discussion

*   **Questions & Ideas:** Have questions or ideas about the digital garden? Open an [Issue](https://github.com/your-community-org/the-foost-digital-garden/issues) in this repository.
*   **General Chat:** Join our [Foost Whatsapp Group] for general discussions, help, and to connect with other contributors!

## 📜 Code of Conduct

We are committed to providing a friendly, safe, and welcoming environment for all. Please read and adhere to our [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

## ⚖️ License

Content contributed to The Foost Digital Garden is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) License](https://creativecommons.org/licenses/by-sa/4.0/). By contributing, you agree that your contributions will be licensed under its terms.

Any underlying code or scripts within this repository (if any) are licensed under the [MIT License](LICENSE_CODE.md)

---

Happy Gardening! We're excited to see what you'll grow. 🌿