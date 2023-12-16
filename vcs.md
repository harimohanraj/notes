[Commits are not snapshots](https://github.blog/2020-12-17-commits-are-snapshots-not-diffs/)
- Git operates on a snapshot model, *not* a diff model.
- Diffs are created to support operations that are more natural with them, i.e. cherry-pick / rebase / patch
- Patches are diffs generated from a snapshot (i.e. commit) that might be applied to a version history that might be actively being worked on by many people, as an alternative (and predecessor) to the typical pull request flow. Patches do not contain "parent history".

[Merging and patches](https://jneem.github.io/merging/) 
- A more mathematical theory of version control, based on patches (diffs?) as opposed to snapshots.

