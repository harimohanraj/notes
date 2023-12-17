[Commits are not snapshots](https://github.blog/2020-12-17-commits-are-snapshots-not-diffs/)
- Git operates on a snapshot model, *not* a diff model.
- Diffs are created to support operations that are more natural with them, i.e. cherry-pick / rebase / patch
- Patches are diffs generated from a snapshot (i.e. commit) that might be applied to a version history that might be actively being worked on by many people, as an alternative (and predecessor) to the typical pull request flow. Patches do not contain "parent history".

[Merging and patches](https://jneem.github.io/merging/) 
- A more mathematical theory of version control, based on patches (diffs?) as opposed to snapshots.
- Patches are line-based, not word-based, but tied to the particular file, which is a list of line indices and their contents?
- Patches can be composed.
- "Merging" is the process of unifying two different representations of a file via patch composition.
- To merge, we need to find two patches (r, s) that bring the file representations (A, B) to a common one (0'). These patches (r, s) must also compose with the patches (p, q) that created (A, B) from (0) such that pr == qs.
  - This implies that (r, s) precisely indicate which information from each file representation and its history is retained in the final merge.  
- However, merges are not unique, and reconciling *what* a merge should produce often requires semantic information about the lines (i.e. which line should come first in a list of instructions?) or requires the user to make a choice.
- Ideally, a merge should be "perfect" / "regretless", meaning 

