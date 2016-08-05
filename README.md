# code0100fun blog

Github pages procedure taken from [this](http://ledtechnica.com/free-ghost-hosting-on-github-pages/) blog post.

## Setup

Install Node 4 or another [supported](http://support.ghost.org/supported-node-versions/) version.

Clone

```bash
$ git clone git://github.com/code0100fun/blog.git
$ cd blog
```

Install

```bash
$ npm install
```

Start

```bash
$ npm start
```

Build

```bash
$ cd static
$ buster generate --domain=http://127.0.0.1:2368
```

Commit

```bash
$ git add -all
$ git commit -m 'Added a new post'
$ git push origin master
```

## Problems

`Reason: Incompatible library version: etree.so requires version 12.0.0 or later, but libxml2.2.dylib provides version 10.0.0`

Answered by this Stack Overflow [question](http://stackoverflow.com/questions/23172384/lxml-runtime-error-reason-incompatible-library-version-etree-so-requires-vers)

```bash
$ brew install libxml2
$ brew install libxslt
$ brew link libxml2 --force
$ brew link libxslt --force
```
