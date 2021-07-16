# Subnero Website

> The future of underwater wireless

[![Build Status](https://travis-ci.com/subnero1/subnero1.github.io.svg?branch=master)](https://travis-ci.com/subnero1/subnero1.github.io)

## Install

1. clone the project: `git clone git@github.com:subnero1/subnero1.github.io.git && cd subnero1.github.io`

## Development

1. build static pages: `jekyll build`
- start local
server: `jekyll serve --config _dev_config.yml --watch`

- if there's error on `invalid byte sequence in US-ASCII
error: invalid byte sequence in US-ASCII`, run the following in the command line:

  ```sh
  LC_CTYPE="en_US.UTF-8"
  LANG="en_US.UTF-8"
  ```
- push to github pages: `git push origin master`
