# Create and applying a patch in git 

## Generate the patch 

```
# in the 1st repo
git diff <commit-id> HEAD > some-changes.patch 
git diff 1a4f HEAD > some-changes.patch
```

## Apply the diff:

```
# in the 2nd repo
git apply /path/to/some-changes.patch
```
