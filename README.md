# DLF 2016 / Jekyll for Librarians

[![https://raw.githubusercontent.com/swat-ds/jekyll-for-librarians/master/assets/img/favicon-96x96.png]](http://ds.swarthmore.edu)

_Roberto Vargas / @betotecario_

_Nabil Kashyap / @_nabilk_

=======

>Projects involving minimal automation would ostensibly afford greater personal or collective awareness of how decisions are made and data is produced

[Jentery Sayers, "Minimal Definitions"](https://go-dh.github.io/mincomp/thoughts/2016/10/02/minimal-definitions/)

### 1) Click the :point_down: Button! :point_down:

[![Nitrous Quickstart](https://nitrous-image-icons.s3.amazonaws.com/quickstart.svg)](https://www.nitrous.io/quickstart?repo=https%3A%2F%2Fgithub.com%2Fswat-ds%2Fjekyll-for-librarians)

This will launch a new Jekyll project on a platform called Nitrous.io, which will ask you to authenticate using your GitHub account. If you'd like to follow along you'll need a [GitHub](https://github.com/) account first.

> One feature of Jekyll is how unopinionated it is about how you develop. Whether you are building a website on your own machine, on a server, or some other configuration. Nitrous.io is an example of an *other*, a cloud based service (unfortunately sunsetting very soon!) that takes advantage of that flexibility, providing a web-based interface for a suitable, consistent environment. [^1]

---

### 2) Explore the file folder `code/jekyll`, which is an example of a vanilla Jekyll installation.

Jekyll makes heavy use of a number of existing web tools, especially [Sass](http://sass-lang.com/guide) and [Liquid Templates](https://github.com/Shopify/liquid/wiki)

Two commands worth exploring are `build` and `serve`. 

> Unlike PHP based CMS (read: Drupal, WordPress, Joomla, Omeka, etc.) Jekyll updates site files only when content is updated, rather than delivering new site files every time the site receives a request.

`$ jekyll build`

The Jekyll library will read some configuration settings then comb through a set of folders, outputting a set of static html files based on the content of those folders. Content is written in [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). Metadata is provided through [YAML front matter](https://jekyllrb.com/docs/frontmatter/).[^2]

`$ jekyll serve --incremental` 

This executes the `build` command but then launches a web server that "watches" for changes. As you edit the files, Jekyll will rebuild based on the files that were edited.

---

### 3) Go ahead and choose `Run > Start jekyll-for-librarians`

Instead of a vanilla install, we have an example of a full-fledged Jekyll theme ([minimal-mistakes](https://github.com/mmistakes/minimal-mistakes)). In addition, behind the scenes we are running the Ruby gem `bundler` to install useful software libraries. These are helpful for development but *not* required to deliver site content. The served site files are good ol' HTML/CSS/JS and nothing else.

---

### 4) How might Jekyll be extended and customized for library uses?

- Using Markdown to edit content rather than baroque WYSIWYG editors with sometimes unpredictable results
- Adding custom metadata for use in Liquid templates to incorporate third party platforms
- Using plaintext metadata to generate low *low* overhead digital exhibits and collections

---

### 5) How do you tie it all together?

These remarks only scratch the surface, if that. Two major questions remain. How do you publish? How might you collaborate?

- Copy (`scp` or `ftp`) `_site` files onto the server (no special permissions or software required)
- Publish using [GitHub Pages](https://pages.github.com/, GitHub's integrated Jekyll implementation
- Or, if feeling plucky, deploy using [git hooks](https://jekyllrb.com/docs/deployment-methods/)
- Even fancier, we might talk about using [GitHub webhooks](https://developer.github.com/webhooks/), e.g. this [PHP based version](https://github.com/dintel/php-github-webhook)
- Or you could possibly combine all of the above, plus a lightweight editing layer over GitHub ([prose.io](http://prose.io/#about)) to maintain a byzantine set of guidelines and documentation, consisting of 1000s of pages, helping guide users through one of [the most complex bureaucracies on earth](https://www.healthcare.gov/).

---

### 6) And relax!

Knowing that even if (ahem) there's no one to maintain the resource, you aren't opening up yourself to security vulnerability or the overhead of a database process or any sweat at all :cold_sweat: in case such a resource needs to be transfered or updated. 

---

[^1]: An developer environment basically describes the combination of an operating system, any programming languages and any software libraries (and their particular versions). Even seemingly small differences can cause surprising differences in software behavior.
[^2]: [YAML Ain't Markup Language](http://yaml.org/)!

---

## Further Resources

- Amanda Visconti, ["Building a static website with Jekyll and GitHub Pages"](http://programminghistorian.org/lessons/building-static-sites-with-jekyll-github-pages). Yet another excellent introduction from Programming Historian.
- Of course [Jekyll Official Site](https://jekyllrb.com/)
- Cloud Cannon's [Jekyll Tips](http://jekyll.tips/)
- [Jekyll Theme Repository](http://www.jekyllthemes.io/)
- Michael Rose, ["How I am using jekyll"](https://mademistakes.com/articles/using-jekyll-2016/). A great overview of more advanced Jekyll-based web development workflows.
