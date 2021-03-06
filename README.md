# Force Tab

[![apm package][apm-ver-link]][releases]
[![travis-ci][travis-ci-badge]][travis-ci]
[![appveyor][appveyor-badge]][appveyor]
[![circle-ci][circle-ci-badge]][circle-ci]
[![david][david-badge]][david]
[![download][dl-badge]][apm-pkg-link]
[![mit][mit-badge]][mit]

I don't know about y'all, but sometimes I just want to insert a tab character and I don't want Atom
to argue with me about it! :angry:

Sometimes I'll try to insert a tab and get snippets inserting a bunch of stuff I don't want, or
autocomplete will try to autocomplete something I don't want, or soft tabs is enabled and I
literally **can't** insert an actual tab character without temporarily disabling the setting &mdash;
which is super annoying!

Enter :boom: [`force-tab`](https://atom.io/packages/force-tab)! :boom:

By default Atom outdents code when you press `shift-tab`, but I absolutely never use that! I always
use `cmd-[`, with `cmd-]` for indenting. If you're like me, and sometimes you just want to insert a
damn tab character, I've made `shift-tab` map to a new command that forcibly inserts a tab or an
appropriate number of spaces if `editor.softTabs` is enabled.

Settings for the package include an option to totally disable honoring `editor.softTabs`. There's
also another command, `force-tab:insert-actual-tab`, that _never_ honors soft tab settings.

**Note:** This fork changes the behavior of the original 
[`force-tab`](https://atom.io/packages/force-tab) package to work when you press `tab` and not 
`shift-tab`. To maintain usage of `tab` to confirm an autocomplete entry, add this to your 
`keymap.cson` file: 

```
'atom-text-editor.autocomplete-active':
  'tab': 'autocomplete-plus:confirm'
```

This is not published on Atom, has not been fully tested to work well for all usages of `tab`, 
and is for personal use.

---

[MIT][mit] © [lexicalunit][author] et [al][contributors]

[mit]:              http://opensource.org/licenses/MIT
[author]:           http://github.com/lexicalunit
[contributors]:     https://github.com/lexicalunit/force-tab/graphs/contributors
[releases]:         https://github.com/lexicalunit/force-tab/releases
[mit-badge]:        https://img.shields.io/apm/l/force-tab.svg
[apm-pkg-link]:     https://atom.io/packages/force-tab
[apm-ver-link]:     https://img.shields.io/apm/v/force-tab.svg
[dl-badge]:         http://img.shields.io/apm/dm/force-tab.svg
[travis-ci-badge]:  https://travis-ci.org/lexicalunit/force-tab.svg?branch=master
[travis-ci]:        https://travis-ci.org/lexicalunit/force-tab
[appveyor]:         https://ci.appveyor.com/project/lexicalunit/force-tab?branch=master
[appveyor-badge]:   https://ci.appveyor.com/api/projects/status/xt11sc0u7qd4tx0m/branch/master?svg=true
[circle-ci]:        https://circleci.com/gh/lexicalunit/force-tab/tree/master
[circle-ci-badge]:  https://circleci.com/gh/lexicalunit/force-tab/tree/master.svg?style=shield
[david-badge]:      https://david-dm.org/lexicalunit/force-tab.svg
[david]:            https://david-dm.org/lexicalunit/force-tab
