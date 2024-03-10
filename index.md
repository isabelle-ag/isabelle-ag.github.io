# Hosting Your Resume on GitHub Pages

## Purpose

This guide provides step-by-step instructions on how to host a resume on GitHub Pages. By following these instructions, you'll be able to showcase your resume online using GitHub's free hosting service.

## Prerequisites

To keep this process simple and streamlined, the only application you will need is your browser.
Additionally, ensure you have the following:

- A resume formatted in Markdown, saved as *index.md*
   - You can use an online Markdown editor like [StackEdit](https://stackedit.io/app#/) to help with syntax.
   - Make sure you (re)name your resume *index.md* or GitHub won't know to use it
- A GitHub account.
   - You can sign up at [GitHub](https://github.com/)

Additional resources can be found in the [Resources Section](#resources)

---

## Instructions

---

### 1. Go to GitHub

- Open GitHub at [github.com](https://github.com).
- If not already logged in, log in to your account.

---

### 2. Create a New Repository

- Click on the **+** icon in the top-right corner of the GitHub webpage and select **New repository**.
- Name your repository *[yourgithubname].github.io*, putting your username in the placeholder.
  
  `*Important:* Convert any uppercase letters in your username to lowercase`
- Make sure the repository is set to public.
- Check the **Initialize this repository with a with README** option.
- Click on the **Create Repository** button.

---

### 3. Upload Your Resume

- You should now be in your new repository's main page, containing only a README.md file.
- To upload a file, click on the **+** button, located in between the **Go to file** and **<> Code** buttons.
- Click **Upload files**.
- Click on the **choose your files** option.
- Navigate to the location of your resume and click upload.
- Write a meaningful commit message, for example: *Uploaded resume as index.md*

---

### 4. Add Configurations

- In order to choose a theme, we need to add a configuration file.
- From the **Code** tab of your repository (located near the top of the page), click on the same **+** button you used to upload your resume.
- Select **Create new file**.
- At the top of the page, name the file *_config.yml*
- Paste the following into the body of the file:

```md
title: <Full Name>
description: 
remote_theme: pages-themes/tactile@v0.2.0
plugins:
- jekyll-remote-theme
```

- Put your full name in the title field.
- Optional: The description field is optional. If you choose to use it, you can put anything there. I recommend having your contact information there. I put *[email] | [github link]*,
- Click on the **Commit changes...** button in the top right of the page
- Write a meaningful commit message, like *Create _config.yml* and click commit.

---

### 5. Enable GitHub Pages

- Navigate to the **Settings** tab of your repository.
- Under the **Code and automation** section on the left, click **Pages**
- Under **Source**, select **Deploy from a branch**.
- Under **Branch**, select **Main** and **/(root)**
- Click on **Save**.

--- 

### 6. Access Your Hosted Resume

- Once GitHub Pages is enabled, you'll see a box with a link to your hosted site.
   - The link should be *https://[username].github.io/*
- Click on the **Visit site** link to view your resume online.

---

### 7. Update Resume

- To make changes, you simply need to update your *index.md* file.
- To keep the process simple, we can make changes directly on the GitHub webpage.
- Navigate to your repository on [GitHub]<https://github.com>, this should be github.com/[username]/[username].github.io
- Click on your *index.md*.
- Once the file has loaded, click the pencil in the top right corner.
- Remember to use Markdown formatting; you can click on the **Preview** tab across the top to preview your changes.
   - The preview can be used to verify your Markdown syntax, but this won't preview the website with the theme, just the file in plain Markdown.
- When you're satisfied with your changes, click **Commit Changes** in the top right.
- It may take a few minutes for the website to update. You can view the progress and verify there are no errors by navigating to the **Actions** tab of your repository.

## Resources

- [Etter's Modern Technical Writing](https://www.amazon.com/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS/)

### Markdown

- [Markdown Tutorial](https://www.markdowntutorial.com/)
- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)

### GitHub

- [GitHub Getting Started](https://docs.github.com/en/get-started/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages/)

---

## FAQs

### Why is Markdown better than a word processor?

Markdown better than a word processor because it offers a simpler and more lightweight syntax compared to traditional word processors, making it easier to create and maintain documents. Additionally, Markdown files are plain text, which means you don't have to worry about compatibility between devices, and they can be easily version-controlled using tools like Git.

### Why is my resume not showing up?

If your resume isn't showing up, follow these troubleshooting steps:

- Double-check that your resume file is named *index.md*.
- Verify that the settings set in [Step 5](#5-enable-github-pages) match those described.
- Check under the **Actions** tab that there are no errors and the build is deployed.
- It may take a few minutes for changes to reflect on your hosted resume. If the issue persists, review the GitHub Pages documentation linked in [Resources](#Resources) for troubleshooting tips.
