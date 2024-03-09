# Hosting Your Resume on GitHub Pages

## Purpose

This guide provides step-by-step instructions on how to host a resume on GitHub Pages. By following these instructions, you'll be able to showcase your resume online using GitHub's free hosting service.

## Prerequisites

Before you begin, ensure you have the following:

- A resume formatted in Markdown, saved as index.md
   - Make sure you rename it to index.md
- A GitHub account.

---

## Instructions

---

### Go to GitHub

- Open GitHub at [github.com](https://github.com).
- If not already logged in, log in to your account.

---

### Create a New Repository

- Click on the **+** icon in the top-right corner of the GitHub webpage and select *New repository*.
- Name your repository *<yourgithubname>.github.io*, putting your username in the placeholder.
  
  `*Important:* Convert any uppercase letters in your username to lowercase`
- Make sure the repository is set to public.
- Check the **Initialize this repository with a with README** option.
- Click on the **Create Repository** button.

---

### Upload Your Resume

- You should now be in your new repository's main page, containing only a README.md file.
- To upload a file, click on the **+** button, located in between the *Go to file* and *<> Code* buttons.
- Click *Upload files*.
- Click on the *choose your files* option.
- Navigate to the location of your resume and click upload.
- Write a meaningful commit message, for example: *Upload index.md*

---

### Add Configurations

- In order to choose a theme, we need to add a configuration file.
- From the *Code* page of your repository, click on the same **+** button you used to upload your resume.
- Select *Create new file*.
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
- Optional: The description field is optional. If you choose to use it, you can put anything there. I recommend having your contact information there. I put *<email> | <github link>*,
- Click on the *Commit changes...* button in the top right of the page
- Write a meaningful commit message, like *Create _config.yml* and click commit.

  ---

### Enable GitHub Pages

- Navigate to the **Settings** tab of your repository.
- Under the **Code and automation** section on the left, click **Pages**
- Under **Source**, select **Deploy from a branch**.
- Under **Branch**, select **Main** and **/(root)**
- Click on **Save**.

--- 

### Access Your Hosted Resume

- Once GitHub Pages is enabled, you'll see a box with a link to your hosted site.
- Click on the **Visit site** link to view your resume online.

---

## More Resources

- [Markdown Tutorial](https://www.markdowntutorial.com/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Etter's Modern Technical Writing](https://www.amazon.com/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS)

---

## FAQs

### Why is Markdown better than a word processor?

Markdown better than a word processor because it offers a simpler and more lightweight syntax compared to traditional word processors, making it easier to create and maintain documents. Additionally, Markdown files are plain text, which means you don't have to worry about compatibility between devices, and they can be easily version-controlled using tools like Git.

### Why is my resume not showing up?

If your resume is not showing up:

- Double-check that your resume file is named correctly and has the ".md" extension.
- Make sure that GitHub Pages is enabled for your repository and that the correct branch is selected as the source for your site. It may take a few minutes for changes to reflect on your hosted resume. If the issue persists, review the GitHub Pages documentation for troubleshooting tips.
