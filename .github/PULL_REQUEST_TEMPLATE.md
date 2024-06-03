<!--
Thank you for opening a PR!

Please fill in relevant details below, deleting the HTML comments (i.e. these sections)
as you go. If a section is not relevant at all feel free to remove it. Similarly, if you
have a different way of presenting the same types of information, feel free not to use
this template.
-->
## Goals of this PR

<!--
Give a brief explanation of what this PR is seeking to achieve and who will be
affected by it. Some examples:

```
This PR should make it easier for developers to add a new subcommand by reducing the
amount of boilerplate code required.
```

```
This PR fixes a user-facing bug with `baz`, filed as issue #12.
```

```
This PR improves our confidence in changes by adding new unit tests for existing
behavior. Specifically, this prevets reocurrance of the issue observed last week
where running the `baz` test after `qux` always passes.
```
-->

## Related context

<!--
If there are existing issues or PRs related to this PR, please begin this section
with links to them, for example:

```
Issues: #12, #24
Previous PR: #25
```

Also link to any documentation, reference materials, technical concepts or historical
context reviewers should be aware of while reviewing this PR.
-->

## Updates made

<!--
Provide a concise explanation of what actually changed in this PR. Use bullet points,
subheadsings, or screenshots if appropriate. For example:

```
Before this PR, the `baz` test would always pass if run after `qux`, because the
`qux` test wasn't fully isolated and sets up state that takes a fast path bypassing
the main `baz` oeprations. Fixing this was not trivial; `qux` cannot be fully
isolated because of the way it interacts with `foo`, `frob`, `bar` and `quxor`.

Instead, this change:

* adds a `resetContext()` method on the subcommand interface;
* calls `resetContext()` during test set-up for all subcommands;
* adds a default implementation of `resetContext()` to all subcommands;
* adds a specific `baz.resetContext()` to break the `qux` dependency; and
* adds documentation for how `resetContext()` should be used.
```
-->

## Notes for reviewers

<!--
List questions or requests you have for the reviewers of this PR, in particular if
you are uncertain about anything, if any approach is new or notable, or if there
are parts of the PR where you want reviewers to focus on specifically.
-->

## Testing

### Automated tests

<!--
List any new or notable automated testing changes here which give you confidence
in this PR.
-->

### Manual testing

<!--
List out scenarios you tested to validate this PR works as expected. Include enough
context for reviewers to be able to walk through your scenarios themselves.
-->
