unwatch-gh-org-repos (ugor)
===========================

[![npm version](https://img.shields.io/npm/v/unwatch-gh-org-repos.svg?style=flat)](https://www.npmjs.com/package/unwatch-gh-org-repos)
[![build status](https://api.travis-ci.org/gedex/unwatch-gh-org-repos.svg)](http://travis-ci.org/gedex/unwatch-gh-org-repos)
[![dependency status](https://david-dm.org/gedex/unwatch-gh-org-repos.svg)](https://david-dm.org/gedex/unwatch-gh-org-repos)

unwatch-gh-org-repos (ugor) is a command line interface to unwatch all GitHub
organization / user repos.

If you're trying to do the opposite, watch all GitHub org repos, try its
enemy, [wagor](https://github.com/gedex/watch-all-gh-org-repos).

## Install

```
$ npm install -g unwatch-gh-org-repos
```

## Usage

Once installed globally, `ugor` should be available from shell.

```
$ ugor -h

  Usage: ugor [options]

  Options:

    -h, --help                         output usage information
    -V, --version                      output the version number
    -t, --token <token>                GitHub token
    -o, --organization <organization>  GitHub organization
```

Once installed, you need to [create personal token](https://help.github.com/articles/creating-an-access-token-for-command-line-use/). An example of unwatch all repos in `GedexTestOrg`:

```
$ ugor -t my-personal-token -o GedexTestOrg

Fetching watched GedexTestOrg repos..
┌────────────────────┬────────────────────────────────────────────────────────────┐
│ Repo               │ Description                                                │
├────────────────────┼────────────────────────────────────────────────────────────┤
│ wp-dummy-plugin    │ Repo used for testing                                      │
├────────────────────┼────────────────────────────────────────────────────────────┤
│ repo-with-milesto… │ Repo used for testing                                      │
└────────────────────┴────────────────────────────────────────────────────────────┘
Found 2 watched repos. Unwatch those? (yes)
Unwatched GedexTestOrg/repo-with-milestone-and-issues successfully
Unwatched GedexTestOrg/wp-dummy-plugin successfully
```

## License

MIT
