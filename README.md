# GitHub Release Test

This repository demonstrates coordinated GitHub release workflows.

## Workflows

### 1. Release Build (`release-build.yml`)
- Creates a draft GitHub release
- Uploads build artifacts (app, docs, config)
- Triggered manually with version input

### 2. Release Lambda (`release-lambda.yml`)
- Finds existing draft release by version
- Adds lambda artifacts to the same release
- Updates release notes with lambda section
- Triggered manually with version input

## Testing Steps

1. Run "Release Build" workflow with version `1.0.0`
2. Check that a draft release is created with build artifacts
3. Run "Release Lambda" workflow with same version `1.0.0`
4. Verify the draft release now contains both build and lambda artifacts
5. Manually publish the release from GitHub UI

## Example Usage

```bash
# After pushing to GitHub, go to Actions tab and:
# 1. Run "Release Build" with version: 1.0.0
# 2. Run "Release Lambda" with version: 1.0.0
# 3. Check Releases tab to see the combined draft
```
