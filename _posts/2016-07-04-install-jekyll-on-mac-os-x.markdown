---
layout: post
title:  "Установка Jekyll на Mac OS X"
date:   2016-07-04 07:46:22
categories: tools
---

Я уже писал о том, [как установить Jekyll на Ubuntu]({% post_url 2015-03-22-jekyll %}).
Пришло время написать об установке на Mac OS X 10.11.4 (El Capitan).

На самом деле все очень просто и пост будет очень короткий.

Устанавливаем свежую версию ``ruby`` (установленная в комплекте 2.0 не подходит):

    $ brew install ruby
    $ ruby --version
    ruby 2.3.1p112 (2016-04-26 revision 54768) [x86_64-darwin15]

Если показывается старая версия -- перезапустите терминал.

Устанавливаем ``bundler``:

    $ gem install bundler
    Fetching: bundler-1.12.5.gem (100%)
    Successfully installed bundler-1.12.5
    Parsing documentation for bundler-1.12.5
    Installing ri documentation for bundler-1.12.5
    Done installing documentation for bundler after 4 seconds
    1 gem installed

Напомню содержимое ``Gemfile``:

    $ cat Gemfile
    source 'https://rubygems.org'
    gem 'github-pages'

Устанавливаем ``Jekyll``:

    $ bundle install
    ...
    $ bundle exec jekyll -v
    jekyll 3.1.6

Done :-)