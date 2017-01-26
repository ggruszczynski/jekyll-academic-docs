# Overview
The following is meant as a more complete set of documentation than the QuickStart guide. If you have not yet completed the QuickStart guide it is recommended that you begin there - as it will provide the necessary steps to setting up your GitHub repository and transferring the source files.

### Software Requirements
In order to edit your Jekyll Academic website locally you will need the following pieces of software:
##### Required
  * Text Editor (Any text editor will do, our favorite is [Atom](https://atom.io/))
  * [GitHub Desktop](https://desktop.github.com/). This is used to sync files between your local computer and the GitHub repository that is acting as your website host.
##### Optional
  * [Jekyll](https://jekyllrb.com/docs/quickstart/)

    <small>Note: If you are intending to use GitHub pages to host Jekyll Academic Sites you do not need to have a local installation of Jekyll, GitHub takes care of that work for you. If you wish to host the site elsewhere, or wish to unlock more powerful features available in Jekyll you may want to consider a local Jekyll installation as well. More detailed instructions can be found on the [Advanced Features](/advanced/) page.</small>

# GitHub Setup

#### Connect your GitHub Repository to GitHub Desktop
* Download GitHub Desktop from https://desktop.github.com/ (skip this step if you already have GitHub Desktop installed)
* Double-click on downloaded file to begin the installation
* While on the Welcome screen click on Continue
* Sign in using your GitHub username and password
* Click Sign In
* Click Continue
* Click Continue one more time
* Click on the plus sign in the upper left-hand corner of the screen to add a repository to Github Desktop
* Click Clone
* Find the `[username].github.io` repository you created earlier and click Clone Repository
* Select the location where you would like to save the local copy of the files from your repository (e.g. Documents)
* Once the clone is finished you can click on the name of the repository on the left-hand side of Github Desktop to see any uncommitted changes (there shouldn’t be any yet)

#### Edit File, Sync Changes
* Make changes to one of your website's pages that is now saved in your local filesystem (ex. open resume.md using a text editor and update the information in the file)
* Save the file you edited
* Open GitHub Desktop
* Click to see Uncommitted Changes (at the top center portion of the screen)
* Add commit message to the summary field that says what changes you made
* Click Commit to Master
* Click Sync
* Refresh the browser window with your website ([username].github.io) and check for changes on the page you edited

*****

# Important Files and Folders
In order to better understand how everything in your site works, there are a few files and folders that you need to be aware of. These files control the main elements of your site, including your logo, bio photo and navigation. Full documentation of the directory structure can be found [here](https://jekyllrb.com/docs/structure/).

* **\_config.yml** - This is your websites main configuration file. It allows you to set a site title, links to your social media accounts as well as a logo and bio photo image.

* **accent.scss** - This file is used to set the colors of your site. The site is set up to accept two colors (highlight, lowlight). The main impact of the color choice  

* **\_posts** - This folder holds all of the posts and presentations for your website. There is one sample post file and one sample presentation file located in this directory by default. The easiest way to create a new post or presentation is to simply copy either the post or presentation file and edit the contents.

* **images/bio-photo.jpg** - This is the photo that appears on the home page of the website. The recommended image size is 200px x 200px.

* **images/logo.png** - If you wish to use a logo for your site, include logo.png in the images folder. You will also need to add logo.png under the 'Logo:' section of the \_config.yml file.

* **\_data/navigation.yml** -This is the file that allows you to manage your navigation elements. By default all available navigation items are shown. If you wish to hide any items, simply delete them from this file.

*****

## Adding Blog posts
To add a new blog post to your site you simply create a new Markdown file by either copying another post file and editing the contents or starting with a blank markdown file. Keep in mind that **Jekyll requires that all posts follow the yyyy-mm-dd-title.md naming convention.**

If you wish to begin with a blank markdown file, you must paste the following YAML front matter at the very beginning of your file.

    ---
    layout: post
    title: Add Your Title Here
    excerpt: "Add an excerpt here, the excerpt will appear underneath the blog title"
    modified: 2016-01-13 20:41:38
    tags: [intro, beginner, jekyll, tutorial]
    comments: true
    category: blog
    ---

The important thing to note is that you need to make sure that the category is set to 'blog'. This ensures that this post will appear on the blog page. You can then add your blog content using Markdown as your markup language for the rest of the file.

## Adding Reveal.js Presentations
In Jekyll Academic presentations are actually set up as posts, and live in the same \_posts folder as your blog posts. They also must use the same file naming convention as posts (yyyy-mm-dd-title.md). The main difference between a blog post and a Reveal.js presentation is the layout and category used in the YAML front matter.

If you wish to begin your Reveal.js presentation with a blank markdown file, you must paste the following YAML front matter at the very beginning of your file.

    ---
    layout: slide
    title: Add Your Title Here
    excerpt: "Add an excerpt here, the excerpt will appear underneath the blog title"
    modified: 2016-01-13 20:41:38
    tags: [intro, beginner, jekyll, tutorial]
    comments: true
    category: presentation
    ---
    <section data-markdown>
    # Add Reveal.js slide content here, following the Reveal.js format
    </section>

Note that Reveal.js presentations must use "slide" as the layout and "presentation" as the category.


## Adding Links to External Presentations
If you would rather use another service, like Google Presentations for your presentations you can still link to them from your Jekyll Academic website. To do so start a new file in your \_posts directory following the same yyyy-mm-dd-title.md file name convention and paste the following YAML front matter into that file.

      ---
      layout: post
      title: Add Your Title Here
      excerpt: "Add an excerpt here, the excerpt will appear underneath the blog title"
      modified: 2016-01-13 20:41:38
      tags: [intro, beginner, jekyll, tutorial]
      comments: true
      category: presentation
      ---
      # Title of Presentation
      ## SubTitle of Presentation
      [Text for Link](html link to presentation)

In the above example you are using the 'post' layout, but giving it a 'presentation' category. This means it will give you a blank post page, but will appear under your list of presentations. The content on this page can be anything, but you will need to at least add a link to wherever your presentation is located.

*****
## Adding or Removing Navigation Items
You may want to add additional navigation items that point to different types of content or individual pages. This can be accomplished by adding a new navigation item. In order to add a new navigation item you will:

1) Copy the folder of an existing navigation item (e.g resume) and paste it into the root directory of your project. Rename this folder with the name of the new navigation item.

2) Navigate to \_data/navigation.yml and add a new navigation item by copying the layout of an existing navigation item.

3) Take a look at some of the existing index.md files for other navigation items. Take note of the 'layout' element declared in the frontmatter. This will help you determine which layout is appropriate for your newly created page (e.g. Page or Resume)

*****

## Understanding Layouts
One of the fundamental elements of Jekyll is the ability to utilize different layouts for different types of pages. The layouts are found in the \_layouts folder. These are .html files that drive the layout of any particular page. For example the 'slide' layout contains all of the necessary includes to power Reveal.js slides. The current available layouts in Jekyll Academic are:

* home - This layout is the layout for the homepage of your website. It automatically includes your 5 most recent blog posts in the space to the right of the social media section.
* page - This layout is used for any individual page, like the 'About Me' page. It is a blank page that can be formatted using Markdown.
* post-index - This layout is used on the blog archive. It lists every blog post chronologically separated by year.
* post - This layout is used for blog posts. It includes a few more functionality elements than the 'page' layout.
* resume - This layout is used for the Resume page.
* presentation-post-index - This layout is identical to the post-index layout except it is used on the presentations index to post all presentations you have on your site in one location, chronologically.
slide - This layout is used for creating a Reveal.js slide deck.
