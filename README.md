# GitHub Workflow run on version tags

For the full list of examples and explanations visit https://git.code-maven.com/


```
git tag v1.00
git push --tags
```

The normal checkout will only check out the current revision (sha) and thus `git log` won't show anything.
When we set git tag and them immediatel push it out then the triggered job will see the tag  using `git tag`.

