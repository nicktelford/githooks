# githooks
_A library of git hooks that you may find useful._

All scripts use POSIX Shell (aka. `/bin/sh`) to maximise portability.

## Usage

Each directory contains a set of different hooks you can use. The name of the
directory is the name of the hook, the name of the file describes what that
particular hook does.

1. Choose a hook you wish to use.
2. Install the hook to `.git/hooks/<name>` where `<name>` is the name of the
   _direcctory_ the hook script came from.

If you wish to use multiple scripts for the same hook, you will want to create
a custom hook that calls each of the selected scripts in turn.

## Available Hooks

### commit-msg

#### well-formed

Validates that the commit message is "well-formed", according to the [official
git guidelines](http://git-scm.com/book/en/v2/Distributed-Git-Contributing-to-a-Project#Commit-Guidelines).

Some of the rules this hook enforces are best-effort, for example ensuring
that the summary is in the imperative tense.

All violations are gathered during validation, and a failure will print a list
of all problems.

