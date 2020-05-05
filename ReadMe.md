UniGrammarRuntimeCore.py [![Unlicensed work](https://raw.githubusercontent.com/unlicense/unlicense.org/master/static/favicon.png)](https://unlicense.org/)
===================
~~![GitLab Build Status](https://gitlab.com/UniGrammar/UniGrammarRuntimeCore.py/badges/master/pipeline.svg)~~
~~![GitLab Coverage](https://gitlab.com/UniGrammar/UniGrammarRuntimeCore.py/badges/master/coverage.svg)~~
[![N∅ dependencies](https://shields.io/badge/-N%E2%88%85_deps!-0F0)
[![Code style: antiflash](https://img.shields.io/badge/code%20style-antiflash-FFF.svg)](https://codeberg.org/KOLANICH-tools/antiflash.py)

Core of UniGrammar runtime contains a common framework with minimal dependencies that can be used when creating or wrapping parser generators without actually using `UniGrammar`. It is needed because if you are using OOP, you still have to have some interface, and it would be better if that interface is compatible to the one used in `UniGrammar`, so we won't have to rewrap stuff again and again. There are no stability guarantees though. You are expected to be able to do necessary changes in your code if you use it.

It is splitted into a separate package because we don't want to require its users to install `UniGrammarRuntime` and its dependencies.

It doesn't use `UniGrammar` package as a namespace because this stuff is incompatible to `pip install -e .` (components installed as `-e` break every other components, an it is probably a bug in python), so it has to have an own name `UniGrammarRuntimeCore`.
