# GitHub Workflow run on version tags

For the full list of examples and explanations visit https://git.code-maven.com/


```
git tag v1.00
git push --tags
```

The normal checkout will only check out the current revision (sha) and thus `git log` won't show anything.
When we set git tag and them immediatel push it out then the triggered job will see the tag  using `git tag`.

If I add a tag. Then commit a change. Push out the change. No CI. Then push out the tag. The CI is triggered and the commit with the tag will be checked out. (not the most recent commit)


```
git tag v1
# Make some changes to README
git commit -m update
git push  # this triggers the regular push job.
git push --tags  # this triggers the tag-job only
```

* make a change
* add a tag
* git push --tag
  This will push out the commit and the tag, but because we did not write the stand-alone `git push`
the current remote branch won't show the new commit. (But we can visit the tag and see the new commit)



