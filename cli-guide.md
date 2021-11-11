# CLI Git Guide

## `git clone`

## `git remote`

## `git log`

## `git add`

## `git status`

## `git commit`

## `git rebase`

Commands:

```text
git checkout <source branch>
git pull upstream <source branch>
git checkout <target branch>
git rebase <source branch>
```

### Manually changing conflict

If there were changes introduced to the same parts of content that you also altered, you will get a conflict. This is what will be printed in your terminal:

```text
Auto-merging team.txt
CONFLICT (content): Merge conflict in team.txt
error: could not apply 1ceecb2... fix(name): incorrect spelling
Resolve all conflicts manually, mark them as resolved with
"git add/rm <conflicted_files>", then run "git rebase --continue".
You can instead skip this commit: run "git rebase --skip".
To abort and get back to the state before "git rebase", run "git rebase --abort".
Could not apply 1ceecb2... fix(name): incorrect spelling
```

### Bulk solving rebase conflicts

If you want to default to the changes on the source, not target, you can use the following command:

```text
git checkout --ours -- <filename>
```

It's worth noting that `--ours` and `--theirs` during a rebase is opposite of a regular `git merge` conflict.

## `git push`

### Push failure

When you have rewritten one or more commits, you will get the following error:

```text
To github.com:cerebrl/git-workshop.git
 ! [rejected]        fix_name-spelling -> fix_name-spelling (non-fast-forward)
error: failed to push some refs to 'github.com:cerebrl/git-workshop.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

## `git reflog`
