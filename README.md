git-remote-rebase
=================

[![NPM Status][npm-img]][npm]
[![Travis Status][test-img]][travis]
[![AppVeyor Status][window-img]][appveyor]
[![Coverage Status][coverage-img]][coveralls]
[![Dependency Status][dependency-img]][david]

[npm]:            https://www.npmjs.org/package/git-remote-rebase
[npm-img]:        https://img.shields.io/npm/v/git-remote-rebase.svg

[travis]:         https://travis-ci.org/blond/git-remote-rebase
[test-img]:       https://img.shields.io/travis/blond/git-remote-rebase.svg?label=tests

[appveyor]:       https://ci.appveyor.com/project/blond/git-remote-rebase
[window-img]:     https://img.shields.io/appveyor/ci/blond/git-remote-rebase.svg?label=windows

[coveralls]:      https://coveralls.io/r/blond/git-remote-rebase
[coverage-img]:   https://img.shields.io/coveralls/blond/git-remote-rebase.svg

[david]:          https://david-dm.org/blond/git-remote-rebase
[dependency-img]: http://img.shields.io/david/blond/git-remote-rebase.svg

Intro
-----

When you want to merge a PR, you click the "Merge Pull Request" button. When you click that button, GitHub will run the merge command with the --no-ff option ([source](https://help.github.com/articles/merging-a-pull-request/)). What this means is you get an additional commit in your git history (even if it's not needed).

This gives you the ability to easily rebase and perform [a fast forward merge](http://ariya.ofilabs.com/2013/09/fast-forward-git-merge.html).

The problem
-----------

When not doing a fast forward merge, your git history looks like this:

![Chaos history](https://cloud.githubusercontent.com/assets/2225579/13229013/d9959a44-d9af-11e5-9e55-96c4efccd3ad.png)

Chaos. This makes it pretty difficult to figure out what code is where and when and how it got there.

When you rebase and only do fast forward merges, you get a git history that looks like this:

![Clean history](https://cloud.githubusercontent.com/assets/2225579/13229113/57876ec8-d9b0-11e5-824e-31f1235c37a2.png)

A nice, clean, straight line. This makes it sooooo much nicer!

Unfortunately, GitHub is silent on whether it will ever allow fast-forward merges for merges by default. So I created this to do it for you!

Install
-------

```
$ npm install --save git-remote-rebase
```

License
-------

MIT © [Andrew Abramov](https://github.com/blond)
