# Advanced Features
The quickstart guide was intended to provide you with the easiest possible setup of Jekyll Academic. The integration with GitHub Pages allows you to fully set up Jekyll Academic without ever installing Jekyll locally. However, many users may wish to make advanced modifications to their site. If you wish to do so, you would benefit from installing Jekyll locally. The following instructions are based on using Mac OSX as your operating system.

## Setting Up Jekyll Locally
GitHub Pages has been designed to work with Jekyll allowing you to upload your 'raw' site files and have GitHub interpret them and create your site. This works well for any user that wants to use GitHub Pages. However, there are additional features that can be utilized if you wish to install Jekyll locally. Local installation allows you to preview the changes made to your site without committing them to GitHub. It also allows you to create new posts from the command line.

To set up Jekyll locally you will need to install the following three things:

* [Ruby](https://www.ruby-lang.org/en/downloads/)
* [RubyGems](https://rubygems.org/pages/download)
* [Jekyll](https://jekyllrb.com/docs/installation/)

### Installing Ruby
Probably the easiest way to install Ruby on a Mac is using [Homebrew](http://brew.sh/). Once you have Homebrew installed you can install ruby using the command `brew install ruby`. If you are using another operating system, or wish to have a more advanced ruby setup, you may find the instructions listed [here](https://www.ruby-lang.org/en/documentation/installation/) useful. After installing ruby on your system you will need to install **RubyGems** this can be completed by following the instructions on the [RubyGems](https://rubygems.org/pages/download) website.
### Installing Jekyll
Jekyll can be installed using RubyGems once you have ruby and RubyGems installed you can install Jekyll using the command `gem install jekyll`.

## Using Jekyll Locally
Jekyll is an incredibly powerful tool. It also has a ton of great documentation written about it already that can be found at the [Jekyll](https://jekyllrb.com/) website. We highly recommend you take a look at that site to get a better idea of the advanced features that are available. Two of the most common Jekyll commands are described below.

* **Jekyll Serve** - The primary advantage of installing Jekyll locally is that it allows you to make updates to your site and preview those changes before pushing them to GitHub. In order to view changes that you are making to your site in a preview development server run `jekyll serve` from your project directory and then navigate to http://localhost:4000/.

* **Jekyll Build** - If you wish to host your website somewhere other than GitHub Pages it will require that you create a site folder containing valid HTML and CSS files. You can do this by running `jekyll build` from the root folder of your project directory. That will result in the creation of a \_site folder. That folder can then be uploaded to the webhost of your choosing.

*****
# Site Structure
We have provided a rudimentary file tree to help you navigate the basic file structure of your site. It is broken down into three risk levels (low, medium, high).

* **Low risk** files are ones that you will need to edit in order to update the basic text on your site, but editing them will not cause any damage to site functionality.
* **Medium risk** files contain HTML layout files and CSS files. You may find a need to edit these files to update the look and layout of your site. However, this is considered a more advanced task, breaking these files could cause your site layout to break.
* **High risk** files are the files used by Jekyll to provide basic functionality to the site, it is unlikely that you will need to edit these files, and doing so could cause your site to stop functioning.
```
      ---------------------------------------------------
      Low Risk:
      ├── index.md
      ├── resume.md
      ├── _config.yml
      ├── accent.scss
      |
      |
      ├── _posts
      │   ├── 2016-07-22-example-presentation.md
      │   └── 2016-07-23-example-post.md
      |
      |
      ├── images
      │   ├── bio-photo.jpg
      │   └── logo.png
      ├── _data
      │   └────── navigation.yml
      ---------------------------------------------------
      Medium Risk:
      ├── _sass
      │       
      ├── _includes
      │   ├── _author-bio.html
      │   ├── _browser-upgrade.html
      │   ├── _cvhead.html
      │   ├── _disqus_comments.html
      │   ├── _feed-footer.html
      │   ├── _footer.html
      │   ├── _head.html
      │   ├── _navigation.html
      │   ├── _open-graph.html
      │   ├── _scripts.html
      │   ├── _social-share.html
      │   └── _toc.html
      ├── _layouts
      │   ├── home.html
      │   ├── page.html
      │   ├── post-index.html
      │   ├── post.html
      │   ├── presentation-post-index.html
      │   ├── resume.html
      │   └── slide.html
      ├── assets 
      │ 
      ---------------------------------------------------
      High Risk:
      ├── favicon.png
      ├── presentations.md
      ├── blog.md
      ├── 404.md
      ├── Gemfile
      ├── Gemfile.lock
      ├── Gruntfile.js
      ├── LICENSE
      ├── README.md

```
