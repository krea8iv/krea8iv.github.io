---
layout: default
title:  "Jekyll Static Site Generator & GitHub Pages Quickstart"
date:   2024-11-10 05:28:09 +0530
categories: markdown
---
# Jekyll Static Site Generator & GitHub Pages Quickstart

<iframe width="560" height="315" src="https://www.youtube.com/embed/fV01b0duZwU?si=86ElYZxo_EZ-7ywu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

[Cloud Native Trainer with Mike](https://www.youtube.com/@cloudnativetrainer)

312 views  13 Oct 2024

I walkthrough the process of creating a GitHub pages website with Jekyll static site generator, showing how to install the required software and tools. I also cover creating the site on GitHub how to work on the site on you local machine before pushing changes to GitHub. I demonstrate how to use the default minima theme and how to swap it out for the Hacker theme.

**Chapters**
- [00:00](https://www.youtube.com/watch?v=fV01b0duZwU&t=0s) Introduction
- [00:02:10](https://www.youtube.com/watch?v=fV01b0duZwU&t=130s) What you need
- [00:04:02](https://www.youtube.com/watch?v=fV01b0duZwU&t=242s) Install Ruby for Windows
- [00:06:56](https://www.youtube.com/watch?v=fV01b0duZwU&t=416s) Install Ruby for macOS 
- [00:08:45](https://www.youtube.com/watch?v=fV01b0duZwU&t=525s) Install Jekyll 
- [00:10:20](https://www.youtube.com/watch?v=fV01b0duZwU&t=620s) Create website on GitHub 
- [00:14:11](https://www.youtube.com/watch?v=fV01b0duZwU&t=851s) Create local Jekyll site with Minima Theme 
- [00:20:36](https://www.youtube.com/watch?v=fV01b0duZwU&t=1236s) Local Jekyll site running on localhost 
- [00:21:37](https://www.youtube.com/watch?v=fV01b0duZwU&t=1297s) Push local site to GitHub Pages 
- [00:22:31](https://www.youtube.com/watch?v=fV01b0duZwU&t=1351s) Site deployment to GitHub Pages with GitHub Actions 
- [00:23:16](https://www.youtube.com/watch?v=fV01b0duZwU&t=1396s) Add content to local Site 
- [00:23:43](https://www.youtube.com/watch?v=fV01b0duZwU&t=1423s) Add pages 
- [00:26:38](https://www.youtube.com/watch?v=fV01b0duZwU&t=1598s) Add blog post 
- [00:28:53](https://www.youtube.com/watch?v=fV01b0duZwU&t=1733s) Change the Theme 
- [00:29:15](https://www.youtube.com/watch?v=fV01b0duZwU&t=1755s) GitHub Pages Supported Themes 
- [00:29:23](https://www.youtube.com/watch?v=fV01b0duZwU&t=1763s) Hacker Theme 
- [00:31:34](https://www.youtube.com/watch?v=fV01b0duZwU&t=1894s) Hacker Theme - Errors 
- [00:33:46](https://www.youtube.com/watch?v=fV01b0duZwU&t=2026s) Customise the Hacker Theme - List Posts on Home page 
- [00:40:40](https://www.youtube.com/watch?v=fV01b0duZwU&t=2440s) Show page links in Hacker Theme 
- [00:45:36](https://www.youtube.com/watch?v=fV01b0duZwU&t=2736s) Push changes to GitHub Pages 
- [00:47:15](https://www.youtube.com/watch?v=fV01b0duZwU&t=2835s) Final result on GitHub Pages 
- [00:47:34](https://www.youtube.com/watch?v=fV01b0duZwU&t=2854s) Summary


## My Notes
Here are my notes after watching the tutorial.

### Links
- [Jekyll Static Site Generator & GitHub Pages Quickstart](https://www.youtube.com/watch?v=fV01b0duZwU)
- [The Final Customized Hacker Theme](https://github.com/mikekelly21/mikekelly21.github.io)
- [Hacker Theme Preview](https://pages-themes.github.io/hacker/)
- [Download Ruby](https://www.ruby-lang.org/en/downloads/)
- [Ruby Installer for Windows](https://rubyinstaller.org/)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Sign Up](https://github.com/signup)
- [Visual Studio Code](https://code.visualstudio.com/)
- [GitHub Pages](https://pages.github.com/)
- [GitHub Pages - Blogging with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll)
- [GiHub Pages Dependencies](https://pages.github.com/versions/)

## Creating a site using Jekyll and GitHub pages
Follow the steps to create a static site using Jekyll and GitHub pages.

### Creating the Github repository for the site 
1. Create a new GitHub repository
1. For the Repository name, enter the username. `krea8iv.github.io`
1. Make the repository public.
1. Click **Create**.
1. Create a new directory on your computer, `mkdir krea8iv.github.io`
1. Change to the directory, `cd krea8iv.github.io`
1. Initiate repo, `git init`
1. Change username and email to krea8iv  
`git config user.name krea8iv`  
`git config user.email krea8iv@yahoo.com`
1. In GitHub, copy the commands to create a new repository on the command line.
1. Paste the commands into the terminal.
1. Select Paste anyway when GitHub displays a warning about pasting multiple lines.
1. Go to the website address https://krea8iv.github.io in the browser. When we create a repo with the user name in GitHub, it will create a website automatically using GitHub actions.
1. Click **Actions** to see the workflow for building the pages and deploying the site.

### Initiating the Jekyll site
2. Create a Jekyll site, `jekyll new --skip-bundle . --force`. We skipped bundle to configure a few settings to install the right version of Jekyll for GitHub pages.
3. Open Visual Studio Code, `code .`
4. Open the `Gemfile`.
5. Comment `# gem "jekyll", "~> 4.3.3"`
6. Uncomment `gem "github-pages", group: :jekyll_plugins`
7. Open the [dependency versions](https://pages.github.com/versions/) page for GitHub in the browser. GitHub supports `jekyll 3.10.0` and github-pages `232`
8. In the Gemfile update the line,`gem "github-pages", group: :jekyll_plugins` to `gem "github-pages", "~> 232", group: :jekyll_plugins`
9.  Save and close the Gemfile.
10. In terminal install the bundle, `bundle install`
11. Open the `Gemfile.lock` file in VSCode.
12. Confirm the version of `github-pages` as `github-pages (~> 232)`
13. Confirm the version of `jekyll` as `jekyll (= 3.10.0)`
14. Open `.gitignore` and add `Gemfile.lock` in a new line.

### Configuring the Jekyll site and adding pages
1.  Open `_config.yml`.
2.  Edit the `title`, `email`, `description`, `github_username` and `twitter_username` and save the file.
3.  To build the site, `bundle exec jekyll serve`
4.  Open the browser to view the Jekyll site at: http://127.0.0.1:4000/
5.  Check the About page, example post, title, description, twitter and github usernames.
6.  After checking press `Ctrl+C` to stop the server.
7.  Copy and paste the `about.markdown` file. Rename it to `contact.markdown`.
8.  Open `contact.markdown` and edit the front matter.
9.  Change title to `contact` and permalink to `/about/contact/`.
10. Replace the contents of the page.
> `## Twitter`
> 
> `Contact me on twitter using @krea8iv`
> 
> `## GitHub`
> 
> `Contact me on GitHub using krea8iv`
> 
1. Save the file and serve the site in the terminal with `bundle exec jekyll serve`
2. Check the Contact page and its URL.

### Adding posts
3. Copy, paste and rename the welcome to jekyll.markdown file in the _posts directory. Use the format `yyyy-mm-dd-first-post.markdown`.
4. Change the title, date, and categories in the frontmatter.
5. Enter the content into the post and save it.
6. Open the site in the browser and check the site.

### Changing theme to hacker
7. Check the GitHub Pages themes from https://pages.github.com/themes/
8. Stop the local Jekyll instance using `Ctrl+C` and entering `Y` twice.
9.  Open config.yml and change `theme:` to `jekyll-theme-hacker`.
10. Change the layout to default in the frontmatter for index, about and contact pages.
11. Save the files and serve the site with `bundle exec jekyll serve`.
12. The theme is applied but the about and contact pages and the posts are not displayed.

### Fixing the layouts
1.  Create a new directory called `_layouts`. Code to override the theme will be here.
2.  Create a file called `index.html`.
3.  Open `index.html` and add frontmatter for the page as `layout:default`.
4.  Open the minima layouts page. https://github.com/jekyll/minima/blob/master/_layouts/home.html
5.  Copy lines from 20 to 39 and paste into `index.html`.
6.  Add <!-- {%raw%} -->`{%- endif -%}`<!-- {%endraw%} --> at the end of the file.
7.  Change `posts.size` to `site.posts.size`
8.  Change `post in posts` to `post in site.posts`
9.  Remove the page title section.
<!-- {% raw %} -->
```
{% -if page.list_title -%}
    <h2 class="post-list-heading">{{ page.list_title }}</h2>
{%- endif -%}
```
<!-- {% endraw %} -->
10. Simplify the post.excerpts. Remove:
<!-- {% raw %} -->
```
{% -if site.show_excerts -%}
{%- endif -%}
```
<!-- {% endraw %} -->
11. Change the `index.markdown` layout to `index`.
12. Open the [default.html](https://github.com/pages-themes/hacker/blob/master/_layouts/default.html) page for the hacker theme from GitHub.
13. Click **Raw** and copy the contents of `default.html`.
14. In the `_layouts` directory, create a new file called `default.html` and paste the content you copied.
15. After the Add this code before the `site.description` block.
 <!-- {% raw %} -->
    ```html
        <section id ="pages">
        {%- for page in site.pages -%}
        <a href="{{ page.url}}">{{ page.title | escape }}</a>&nbsp;
        {%- endfor -%}
        </section>
    ```
 <!-- {% endraw %} -->
16.  Stop the Jekyll server. Add, commit and push the changes to the site.
17.  Check the website in the browser.


