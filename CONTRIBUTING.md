# How to contribute

Contributions are always welcome!

Development happens on GitHub, so you can contribute by opening an issue or filing a pull request.

Please open an issue before spending a lot of time on a pull request, especially if you're planning to implement a new feature, or make significant changes to code structure. Those things should be discussed before a PR is opened.

## Commit messages

Always write a clear log message for your commits. One-line messages are fine for small changes, but bigger changes should explain _why_ a change is being made, and anything notable about the change itself.
Commit messages should tell a story, and longer messages are preferred where helpful.

Commit messages should use "50/72" wrapping, that is:
 
 * the first line should be <= 50 characters and a summary of the change; and
 * the remainder of the message should be word-wrapped so the longest line is no more than 72 characters.

Line endings (including at the end of wrapped lines) should be UNIX-style (i.e. `\n` only). 

[Conventional commit](https://www.conventionalcommits.org/en/v1.0.0/) messages are welcome, but not consistently used in this repository.

Similarly, use of markdown where appropriate is appreciated, but not required.

When an issue is fixed by a commit, appropriate [GitHub keywords](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/using-keywords-in-issues-and-pull-requests) should be used to refer to the issue, generally on its own line at the end of the message.

An example of the preferred format for commit messages is:

```console
Refactor `foo` to align with other subcommands

Before this commit, `foo` was an outlier in the way this program
operates. Other subcommands generally have one code file per operation,
whereas `foo` had all of its operations in a single file. It also used
the phrase "do a frob" rather than the word "frobinate", although only
the latter is used elsewhere.

This commit adds unit tests for the following simple foo behaviors:

 * frobinate before `bar` is called;
 * barification of a `foo`, after frobination; and
 * invalidly calling `foo` with an XML string.

In addition, the `foo` module was refactored, and "do a frob" was
changed to "frobinate" in all user-facing locations. Changing this
language in code was too complex, given the cross-dependency on baz, but
fixing this has been filed as issue #42.

Closes #12.
```

## Testing

Please write unit tests for any contributions if doing so is relatively straightforward. It is unlikely that pull requests for new features will be accepted without tests.

If you are fixing a bug, unit tests to prevent regression are appreciated. Even if you don't have a fix, a PR with a failing test (where failure is caused by the bug) is a great help in developing a fix.
