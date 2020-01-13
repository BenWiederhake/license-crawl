# license-crawl

> GitHub's automatic licenses, as a repo, for your convenience.

I usually create repos and gitignores myself, but then use GitHub's
"create repository with a license" feature.
I have no idea why they thought it's a great idea that choosing a
license is bound to repo creation, and cannot be done in the second or
third commit.

So I made this repo, to have the license texts available as files.

## Table of Contents

- [Usage](#usage)
- [FAQ](#faq)
- [TODOs](#todos)
- [NOTDOs](#notdos)
- [Contribute](#contribute)
- [License](#license)

## Usage

Clone this repo to an easily accessible folder, like this:

```
~$ mkdir -p workspace && cd workspace
~/workspace$ git clone https://github.com/BenWiederhake/license-crawl.git
Cloning into 'license-crawl'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
```

And now you don't need GitHub anymore to add a license on top:

```
~/workspace$ mkdir myfancyproject
~/workspace/myfancyproject$ git init
Initialized empty Git repository in ~/workspace/myfancyproject/.git/
~/workspace/myfancyproject$ cp ~/workspace/myfancyproject/unlicense/LICENSE .
~/workspace/myfancyproject$ head LICENSE
This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
```

## FAQ

### Why not just use `/usr/share/common-licenses/` ?

Because these ones are nicer:

```
$ diff -su /usr/share/common-licenses/GPL-3 gnugpl3/LICENSE 
--- /usr/share/common-licenses/GPL-3	2007-07-02 00:55:35.000000000 +0200
+++ gnugpl3/LICENSE	2020-01-13 18:50:30.551660465 +0100
@@ -1,7 +1,7 @@
                     GNU GENERAL PUBLIC LICENSE
                        Version 3, 29 June 2007
 
- Copyright (C) 2007 Free Software Foundation, Inc. <http://fsf.org/>
+ Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
```

Also, it lacks the unlicense, which GitHub apparently recommends over CC0.
I don't really know about the differences.

### Don't you mean "crawler"?

No.  There is no crawler.  Or rather, I *am* the crawler, and crawled these licenses by hand.

This repository is the *result* of the crawling process.

### What's with the `LICENSE.template` files?

Apparently, these licenses require that you fill in your own data (year and name).
That seems to be the only part that needs adaption.  However, it should be fairly
obvious from the file name that *some* adaption is required.

## TODOs

* Add all the other licenses from GitHub
* Add some licenses not on GitHub?
* Make it public
* Become world-famous for spending an hour to simplify this three-second task

## NOTDOs

Here are some things this project will definitely not support:
* Silly licenses or those that I deem bad ideas (most prominently WTFPL)
* Automation, templating, and generally filling in your data.

## Contribute

Feel free to dive in! [Open an issue](https://github.com/BenWiederhake/license-crawl/issues/new) or submit PRs.

## License

I don't think this work is copyrightable, but just in case: Do whatever the fuck you want.
This work is licensed under The Unlicense (see the file `LICENSE`).
