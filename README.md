# comet.dlsu.edu.ph hosted on GitHub Pages

[![Build Status](https://travis-ci.com/dlsucomet/dlsucomet.github.io.svg?token=aXBso18Mo8NKPJy6Yfxs&branch=master)](https://travis-ci.com/dlsucomet/dlsucomet.github.io)

This is the repository for the website of the DLSU Center for Complexity and Emerging Technologies. This is maintained by the center's Strategic Communications team and is powered by [Jekyll](https://jekyllrb.com/). 

## Dependencies

Here are the dependencies for this website. You can also check the `Gemfile` for more
information: 

- Ruby==2.5.3
- gem==2.7.6
- jekyll=3.5.2
- minima==2.5.0
- html-proofer
- jekyll-sitemap
- jekyll-feed==0.6
- jekyll-seo-tag

## Set-up

We're working on a macOS and here are some quick instructions to get things started.

Install the bundler and jekyll gems in your system:

```
$ gem install bundler jekyll
```

Then, install the dependencies included in your `Gemfile` and `_config.yml`, and call `jekyll serve`:

```
$ git clone https://github.com/dlsucomet/dlsucomet.github.io.git 
$ cd dlsucomet.github.io/
$ bundle install
$ bundle exec jekyll serve
```

You now have a local instance of your Jekyll website that you can access at `localhost:4000`.