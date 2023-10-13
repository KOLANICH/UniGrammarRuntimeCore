UniGrammarRuntimeCore.py [![Unlicensed work](https://raw.githubusercontent.com/unlicense/unlicense.org/master/static/favicon.png)](https://unlicense.org/)
===================
~~![GitLab Build Status](https://gitlab.com/UniGrammar/UniGrammarRuntimeCore.py/badges/master/pipeline.svg)~~
~~![GitLab Coverage](https://gitlab.com/UniGrammar/UniGrammarRuntimeCore.py/badges/master/coverage.svg)~~
[![N∅ dependencies](https://shields.io/badge/-N%E2%88%85_deps!-0F0)
[![Code style: antiflash](https://img.shields.io/badge/code%20style-antiflash-FFF.svg)](https://codeberg.org/KOLANICH-tools/antiflash.py)

**We have moved to https://codeberg.org/UniGrammar/UniGrammarRuntimeCore.py, grab new versions there.**

Under the disguise of "better security" Micro$oft-owned GitHub has [discriminated users of 1FA passwords](https://github.blog/2023-03-09-raising-the-bar-for-software-security-github-2fa-begins-march-13/) while having commercial interest in success and wide adoption of [FIDO 1FA specifications](https://fidoalliance.org/specifications/download/) and [Windows Hello implementation](https://support.microsoft.com/en-us/windows/passkeys-in-windows-301c8944-5ea2-452b-9886-97e4d2ef4422) which [it promotes as a replacement for passwords](https://github.blog/2023-07-12-introducing-passwordless-authentication-on-github-com/). It will result in dire consequencies and is competely inacceptable, [read why](https://codeberg.org/KOLANICH/Fuck-GuanTEEnomo).

If you don't want to participate in harming yourself, it is recommended to follow the lead and migrate somewhere away of GitHub and Micro$oft. Here is [the list of alternatives and rationales to do it](https://github.com/orgs/community/discussions/49869). If they delete the discussion, there are certain well-known places where you can get a copy of it. [Read why you should also leave GitHub](https://codeberg.org/KOLANICH/Fuck-GuanTEEnomo).

---

Core of UniGrammar runtime contains a common framework with minimal dependencies that can be used when creating or wrapping parser generators without actually using `UniGrammar`. It is needed because if you are using OOP, you still have to have some interface, and it would be better if that interface is compatible to the one used in `UniGrammar`, so we won't have to rewrap stuff again and again. There are no stability guarantees though. You are expected to be able to do necessary changes in your code if you use it.

It is splitted into a separate package because we don't want to require its users to install `UniGrammarRuntime` and its dependencies.

It doesn't use `UniGrammar` package as a namespace because this stuff is incompatible to `pip install -e .` (components installed as `-e` break every other components, an it is probably a bug in python), so it has to have an own name `UniGrammarRuntimeCore`.
