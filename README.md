# jekyll-blog-demo

Jekyll Blog Demo Project
---

### Contents
- [Requirements](#requirements)
- [Setup](#setup)
- [Checklist](#checklist)
- [Extra Credit](#extra-credit)

---

## Requirements

- [x] `git`
  - *Should already be setup*
  - *Should clone/push using SSH auth [(more info)](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh)*
- [ ] `ruby`
  - *Expected version: `2.7.5`*
  - *Minimum version: `2.6.x`*
  - *See [rbenv](https://github.com/rbenv/rbenv) or [rvm](https://rvm.io) install versions (optional)*
- [ ] `jekyll` + `bundler`
  - *Installed as a gems:* `gem install jekyll bundler`
  - [More info on Jekyll](https://jekyllrb.com)

---

## Setup

1) Fork this repo
    - From demo repo page, click `Fork` button near top right:
    ![pre fork](assets/img/pre-fork.png)
    - Select **your username** and wait for fork to be created
    - After fork is created, you will be on page with new repo *(example below)*
    ![post fork](assets/img/post-fork.png)
2. Clone repo from your fork
    - Select `Code` dropdown and copy clone url using SSH
    - *[Click here to learn about SSH keys on GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh)*
    ![clone ssh](assets/img/clone-ssh.png)
    - Navigate to desired parent workinig directory
    ```bash
    cd ~/development # or wherever you want to save your local repo
    ```
    - Paste copied clone url to clone repo *(or clone with git GUI)*
    ```bash
    git clone git@github.com:myusername/jekyll-blog-demo
    ```
3. Open local repo directory
    - Change directories into newly cloned repo dir:
    ```bash
    cd jekyll-blog-demo
    ```
4. Install dependencies
    - *This will install all gems specified in `Gemfile`*
    ```bash
    bundle install
    ```
5. Run local Jekyll dev server
    - *You can add omit the `--livereload` to restart manually on updates*
    ```bash
    bundle exec jekyll serve --livereload
    ```
6. Visit local dev url
    - Open [http://localhost:4000](http://localhost:4000) in your browser
    - *Local dev port can be changed if needed. [(see config options here)](https://jekyllrb.com/docs/configuration/options/)*

---

## Checklist

- [x] New Jekyll Project
  - *Already done, this repo is a fresh `jekyll new ...` project*
  - See [https://jekyllrb.com/docs](https://jekyllrb.com/docs) for more info
- [ ] Review expected file usage & structure
  - `page` uses `layout`
  - `page` `layout` contains an `include` for listing items
  - each `item` is output to a new `layout`
- [ ] Build a collection of content block items
  - Each content block item should have a `title` and `subtitle` in the `frontmatter` and some lorem in the main content (below the frontmatter)
  - Each content block item should also have a `published` setting in the frontmatter
    - *This should be a `boolean` field type (values: `true` | `false`)*
    - **Note:** *`yaml` [supports a wide range of "valid" boolean values](https://yaml.org/type/bool.html)*, but `true` / `false` is most common.
- [ ] In a new section (or include snippet), loop through each item in your collection and output them into content blocks, omitting any blocks whose `published` setting is `false`.
- [ ] Create a page to hold that section (homepage is fine) and render into the browser.
  - **Note: Don't forget to export the `collection`, `section` and `page` from the `_config.yml`**
  - See [https://jekyllrb.com/docs](https://jekyllrb.com/docs) for more info
- [ ] Create several *(at least 3)* items (posts) under your new collection
  - At least 1 where: `published=true`
  - At least 1 where: `published=false`
  - Test different data/values in "frontmatter" and content blocks
- [ ] Commit changes *(can use a new/custom branch name)*
- [ ] Push changes *(to **your** forked repo)*
- [ ] Open a pull request against this repo (`bowtie-co/jekyll-blog-demo`)
- [ ] Add any additional info and/or questions you might have

---

## Extra Credit

- [ ] Add/update more collections, templates, includes, styles, etc
  - Aim to demonstrate deeper understanding of the patterns & technologies
- [ ] Setup & utilize [bootstrap framework](https://getbootstrap.com/)
  - Improve and customize styles, responsiveness, etc
- [ ] Add new/custom [jekyll plugins](https://jekyllrb.com/docs/plugins/)
- [ ] Build and deploy static site as demo
  ```bash
  # Build compiled static site (default out dir: "_site")
  bundle exec jekyll build
  # Copy/deploy contents from _site/* to web server/provider
  ```
- [ ] Add [support for docker development](https://www.docker.com/)
  - Create `Dockerfile` + `docker-compose.yml` files
  - Define jekyll demo builds in containerized envs
  - Running `docker-compose up` starts the app (same as `jekyll start`)
