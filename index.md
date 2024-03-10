# Hosting Your Resume on GitHub Pages

`Audience: Beginners`

### Contents:

 - [Purpose](#Purpose)
 - [Lessons From Etter](#Lessons-from-etter)
 - [Instructions](#Instructions)
 - [Resources](#Resources)
 - [FAQs](#FAQs)

---

## Purpose

This guide provides step-by-step instructions on how to host a resume on GitHub Pages while adhering to the general principles of technical writing as explained in Andrew Etter's book, [Modern Technical Writing: An Introduction to Software Documentation](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS). By following these principles, we ensure clarity and effectiveness in our instructions for hosting your resume on GitHub Pages.

## Lessons from Etter

### Tools

The tools we will use that Etter describes in his book are GitHub, GitHub Pages, Jekyll, and Markdown.

To highlight some of the key principles from *Modern Technical Writing* that we'll follow in this guide.

### Define the Audience

It's crucial to define your audience before you begin writing. The vocabulary, steps, and presentation should cater to your audience.
The audience for this guide is beginners; we'll use simple language and avoid technical jargon.

The audience for your resume will be different. Take time to consider your audience so you can properly tailor your resume. 
> Etter highlights the importance of this consideration in his book: “a single inaccurate assumption about your audience can lead to a mountain of discarded work”.

### Consistency in Style

For clarity and professionalism, consistency is essential. Inconsistencies may make you appear as an untrustworthy source.
We strive for consistency in our formatting:

- Buttons you click are **in bold**.
- Text to input is *in italics*.
- Placeholder text for the user to replace is [in square brackets].
> Additional information will be in blockquotes.

Furthermore, we use headings to ensure this guide is easy to follow.

### Build a Static Website

Hosting your resume on a website rather than sending it as a PDF has several benefits.

- You can make changes at any time, rather than having to send an updated version of your resume each time.
- Elimiates compatibility issues.
- Easy to share, all you need to send is the link!

Etter advocates for using static websites over dynamic ones where possible for many reasons, including the simplicity to create and maintain, requiring only the GitHub webpage. Additionally, static sites are much quicker to load and are far more beginner friendly.

### Use Distributed Version Control

Etter argues that distributed version control systems, like GitHub, are essential. GitHub allows for simple editing, remote access, ease in repairing mistakes and collaboration, and will host our site for us!

## Prerequisites

To keep this process simple and streamlined, the only application you will need is your browser.
Additionally, ensure you have the following:

- A resume formatted in Markdown, saved as *index.md*.
   - You can use an online Markdown editor like [StackEdit](https://stackedit.io/app#/) to help with syntax.
   - Make sure you (re)name your resume *index.md* or GitHub won't know to use it.
- A GitHub account.
   - You can sign up at [github.com](https://github.com/).

Additional resources can be found in the [Resources Section](#resources).

---



## Instructions

### 1. Go to GitHub

- Open GitHub at [github.com](https://github.com).
- If not already logged in, log in to your account.

---

### 2. Create a New Repository

- Click on the **+** icon in the top-right corner of the GitHub webpage and select **New repository**.
- Name your repository *[yourgithubname].github.io*, putting your username in the placeholder.
  
  `Important: Convert any uppercase letters in your username to lowercase when creating your repository.`
- Make sure the repository is set to public.
- Check the **Initialize this repository with a with README** option.
- Click on the **Create Repository** button.

  ![Create Repository](/images/CreateRepo.png)

---

### 3. Upload Your Resume

- You should now be in your new repository's main page, containing only a README.md file.
- To upload a file, click on the **+** button, located in between the **Go to file** and **<> Code** buttons.
- Click **Upload files**.
- Click on the **choose your files** option.
- Navigate to the location of your resume and click upload.
- Write a meaningful commit message, for example: *Uploaded resume as index.md*.

---

### 4. Enable GitHub Pages

- Navigate to the **Settings** tab of your repository.
- Under the **Code and automation** section on the left, click **Pages**.
- Under **Source**, select **Deploy from a branch**.
- Under **Branch**, select **Main** and **/(root)**.
- Make sure your settings match those in the image below.
- Click on **Save**.

![Pages Settings](/images/pagesSettings.png)

--- 

### 5. Add Configurations

By default, GitHub works with Jekyll, a static site generator that will simplify the process for us. The only thing left is to customize our site and make our resume appear more professional. For more information, refer to [Jekyll](https://jekyllrb.com).

- In order to set a theme, we need to add a configuration file.
- From the **Code** tab of your repository (located near the top of the page), click on the same **+** button you used to upload your resume.
- Select **Create new file**.
- At the top of the page, name the file *_config.yml*.
    > The _config.yml file is a YAML configuration file used by Jekyll, the engine behind GitHub Pages. This allows users to specify settings and customize their site.
- Paste the following into the body of the file:

```md
title: [Page Title]
description: 
remote_theme: pages-themes/tactile@v0.2.0
plugins:
- jekyll-remote-theme
```

- Set your page title, I recommend using your full name.
- Optional: The description field is optional. If you choose to use it, you can put anything there. I recommend having your contact information there. I put *[email] | [github link]*,
- Click on the **Commit changes...** button in the top right of the page.
- Write a meaningful commit message, like *Create _config.yml* and click commit.

---

### 6. Access Your Hosted Resume

- Once GitHub Pages is enabled, you'll see a box with a link to your hosted site.
   - The link should be *https://[username].github.io/*,
- Click on the **Visit site** link to view your resume online.

Now your resume should be live:

![Hosted resume gif](/images/hostedSite.gif)

---

### 7. Update Resume

- To make changes, you simply need to update your *index.md* file.
- To keep the process simple, we can make changes directly on the GitHub webpage.
- Navigate to your repository on [GitHub](https://github.com), this should be github.com/[username]/[username].github.io.
- Click on your *index.md*.
- Once the file has loaded, click the pencil in the top right corner.
- Remember to use Markdown formatting; you can click on the **Preview** tab across the top to preview your changes.
    > Before committing changes to your resume file, it's helpful to preview them to verify your changes. While GitHub provides a preview tab for viewing Markdown syntax, it's important to note that this preview won't display the site with the chosen theme. However, it can still be useful for verifying the correctness of Markdown formatting, as seen below.

 ![Plain markdown preview](/images/mdpreview.png)

- When you're satisfied with your changes, click **Commit Changes** in the top right.
- It may take a few minutes for the website to update. You can view the progress and verify there are no errors by navigating to the **Actions** tab of your repository.

## Resources

- Etter's [Modern Technical Writing](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS)

### Markdown

- [Markdown Tutorial](https://www.markdowntutorial.com/)
- [Markdown Guide](https://www.markdownguide.org)
- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)

### GitHub

- [GitHub Getting Started](https://docs.github.com/en/get-started/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages/)

---

## FAQs

### Why is Markdown better than a word processor?

Markdown is a lightweight markup language that allows users to format text using simple syntax. It's preferred for creating documents like resumes because it offers several benefits:
- **Simplicity**: Markdown syntax is straightforward and easy to learn, making it accessible to users with varying levels of technical knowledge.
- **Compatibility**: Markdown files are plain text, ensuring compatibility across different devices and platforms. 
- **Version Control**: Markdown files can be easily version-controlled using tools like Git, allowing users to track changes and collaborate effectively.


### Why is my resume not showing up?

If your resume isn't showing up, follow these troubleshooting steps:

### General Troubleshooting

- **Check File Names**: Ensure that your resume file is named correctly as `index.md`. File names are case-sensitive, so make sure it matches exactly.
- **Verify Repository Settings**: Double-check that the settings configured in [Step 5](#5-enable-github-pages) match those described in the instructions.
   - Ensure that the repository is set to public and the correct branch is selected.
- **Check Deployment Progress**: Check under the **Actions** tab that there are no errors and the build is deployed.
- It may take a few minutes for changes to reflect on your hosted resume. If the issue persists, review the GitHub Pages documentation linked in [Resources](#Resources) for troubleshooting tips.

---

## Acknowledgements

- [BarbzCodez](https://github.com/BarbzCodez) for editing
- [Andrew Etter](https://andyetter.com) for his book [Modern Technical Writing](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS)
- Jekyll theme [Tactile](https://github.com/pages-themes/tactile)

## Author

Isabelle Anderson-Gregoire
[/isabelle-ag](https://github.com/isabelle-ag)
