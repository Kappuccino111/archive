# Archives for Kappuccino111

This repository contains the code for my personal brain dump.

The website was created as an experiment to learn a little about SASS and Jekyll and how ruby-based static site generators work, when I was in college.

Jekyll was used a getting started tool and then the fancy layout is primarily SASS/CSS.

The original version of this site was hosted on vercel. However having got bored of the normal netlify.app / vercel.app / github.io domains I finally decided to study
a bit more about how DNS, hosting and routing are set up. This in turn made me take on a nearly 2 year old abandoned project, modify it a little bit and configure it for hosting.

Due to lack of a resources currently the layout is limited to static site generation and cross linking the free github.io extension to my personal domain.

I will hopefully be writing about this a little bit more in a blog (maybe).

If there is interest I may also create a template repository (no estimated ETA on that). For now the set up is as follows:
- git clone this repository (and optionally remove the .git, _articles folders to start fresh)
- [Install jekyll](https://jekyllrb.com/docs/installation/) and bundler gems
- Run `bundle install` to install dependencies
- Run `bundle exec jekyll serve` to start a local server at `http://localhost:4000`
- Modify the `_config.yml` file to change site settings
- Add posts to the '_articles' folder in markdown format, with the layout specified in the front matter
- Customize the SASS files in the `assets/css` folder to change the site's appearance
